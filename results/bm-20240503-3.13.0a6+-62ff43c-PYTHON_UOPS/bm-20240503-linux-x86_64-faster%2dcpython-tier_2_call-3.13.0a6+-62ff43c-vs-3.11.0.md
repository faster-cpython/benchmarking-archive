# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 62ff43c
- commit date: 2024-05-03
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 327 ms: 1.24x slower                                                    |
| chameleon      | 6.70 ms                                                | 8.06 ms: 1.20x slower                                                   |
| html5lib       | 64.8 ms                                                | 77.8 ms: 1.20x slower                                                   |
| tornado_http   | 98.1 ms                                                | 105 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                  | 1.18x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 358 ms: 1.37x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 468 ms: 1.34x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 976 ms: 1.33x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 985 ms: 1.31x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 512 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 631 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 640 ms: 1.17x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 196 ms: 1.01x slower                                                    |
| float          | 78.9 ms                                                | 90.6 ms: 1.15x slower                                                   |
| nbody          | 96.0 ms                                                | 122 ms: 1.27x slower                                                    |
| Geometric mean | (ref)                                                  | 1.14x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                   |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                    |
| regex_v8       | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                   |
| regex_compile  | 141 ms                                                 | 190 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 11.1 ms: 1.20x faster                                                   |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                    |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.0 us: 1.02x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.23 us: 1.00x slower                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 111 ms: 1.02x slower                                                    |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.13 us: 1.12x slower                                                   |
| unpickle             | 13.8 us                                                | 15.7 us: 1.14x slower                                                   |
| tomli_loads          | 2.30 sec                                               | 2.65 sec: 1.15x slower                                                  |
| unpickle_pure_python | 242 us                                                 | 285 us: 1.18x slower                                                    |
| xml_etree_process    | 56.9 ms                                                | 68.4 ms: 1.20x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 97.6 ms: 1.20x slower                                                   |
| pickle_pure_python   | 320 us                                                 | 405 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.23 ms: 1.20x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 14.0 ms: 1.31x slower                                                   |
| django_template | 33.5 ms                                                | 44.5 ms: 1.33x slower                                                   |
| genshi_xml      | 53.4 ms                                                | 72.9 ms: 1.36x slower                                                   |
| genshi_text     | 22.5 ms                                                | 32.0 ms: 1.42x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.35x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 194 us: 2.68x faster                                                    |
| generators                 | 74.9 ms                                                | 30.6 ms: 2.45x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 532 ms: 1.65x faster                                                    |
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 358 ms: 1.37x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 468 ms: 1.34x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 976 ms: 1.33x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 985 ms: 1.31x faster                                                    |
| pylint                     | 476 ms                                                 | 367 ms: 1.30x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 512 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 631 ms: 1.21x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 11.1 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 640 ms: 1.17x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 3.62 ms: 1.11x faster                                                   |
| coroutines                 | 27.0 ms                                                | 24.9 ms: 1.08x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                    |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                                   |
| pickle_dict                | 34.6 us                                                | 34.0 us: 1.02x faster                                                   |
| unpickle_list              | 5.21 us                                                | 5.23 us: 1.00x slower                                                   |
| pidigits                   | 194 ms                                                 | 196 ms: 1.01x slower                                                    |
| mdp                        | 2.77 sec                                               | 2.81 sec: 1.01x slower                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 111 ms: 1.02x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                   |
| logging_simple             | 6.22 us                                                | 6.55 us: 1.05x slower                                                   |
| comprehensions             | 23.6 us                                                | 25.1 us: 1.06x slower                                                   |
| logging_format             | 6.81 us                                                | 7.30 us: 1.07x slower                                                   |
| raytrace                   | 309 ms                                                 | 331 ms: 1.07x slower                                                    |
| tornado_http               | 98.1 ms                                                | 105 ms: 1.07x slower                                                    |
| richards_super             | 61.9 ms                                                | 66.6 ms: 1.08x slower                                                   |
| dask                       | 365 ms                                                 | 393 ms: 1.08x slower                                                    |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                   |
| thrift                     | 784 us                                                 | 851 us: 1.09x slower                                                    |
| sympy_sum                  | 169 ms                                                 | 184 ms: 1.09x slower                                                    |
| bench_thread_pool          | 834 us                                                 | 914 us: 1.10x slower                                                    |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                    |
| deltablue                  | 3.92 ms                                                | 4.37 ms: 1.11x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.13 us: 1.12x slower                                                   |
| meteor_contest             | 109 ms                                                 | 123 ms: 1.13x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.14x slower                                                   |
| aiohttp                    | 1.12 ms                                                | 1.28 ms: 1.15x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.38 ms: 1.15x slower                                                   |
| float                      | 78.9 ms                                                | 90.6 ms: 1.15x slower                                                   |
| tomli_loads                | 2.30 sec                                               | 2.65 sec: 1.15x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 24.8 ms: 1.16x slower                                                   |
| sympy_str                  | 297 ms                                                 | 344 ms: 1.16x slower                                                    |
| sqlite_synth               | 2.57 us                                                | 3.00 us: 1.17x slower                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.67 ms: 1.17x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 75.5 ms: 1.17x slower                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 2.05 ms: 1.17x slower                                                   |
| chaos                      | 71.9 ms                                                | 84.4 ms: 1.17x slower                                                   |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                                   |
| unpickle_pure_python       | 242 us                                                 | 285 us: 1.18x slower                                                    |
| sympy_expand               | 484 ms                                                 | 578 ms: 1.19x slower                                                    |
| richards                   | 49.8 ms                                                | 59.4 ms: 1.19x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.84 us: 1.19x slower                                                   |
| pycparser                  | 1.19 sec                                               | 1.42 sec: 1.20x slower                                                  |
| crypto_pyaes               | 76.7 ms                                                | 91.9 ms: 1.20x slower                                                   |
| html5lib                   | 64.8 ms                                                | 77.8 ms: 1.20x slower                                                   |
| fannkuch                   | 405 ms                                                 | 487 ms: 1.20x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 7.23 ms: 1.20x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 68.4 ms: 1.20x slower                                                   |
| chameleon                  | 6.70 ms                                                | 8.06 ms: 1.20x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 97.6 ms: 1.20x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 66.6 ms: 1.20x slower                                                   |
| sqlglot_normalize          | 113 ms                                                 | 137 ms: 1.21x slower                                                    |
| go                         | 149 ms                                                 | 181 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.17 ms: 1.23x slower                                                   |
| 2to3                       | 264 ms                                                 | 327 ms: 1.24x slower                                                    |
| nqueens                    | 87.9 ms                                                | 109 ms: 1.24x slower                                                    |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| mypy2                      | 686 ms                                                 | 859 ms: 1.25x slower                                                    |
| deepcopy                   | 365 us                                                 | 459 us: 1.26x slower                                                    |
| async_generators           | 374 ms                                                 | 471 ms: 1.26x slower                                                    |
| pickle_pure_python         | 320 us                                                 | 405 us: 1.26x slower                                                    |
| nbody                      | 96.0 ms                                                | 122 ms: 1.27x slower                                                    |
| scimark_monte_carlo        | 70.7 ms                                                | 90.1 ms: 1.27x slower                                                   |
| deepcopy_memo              | 40.2 us                                                | 51.4 us: 1.28x slower                                                   |
| scimark_fft                | 345 ms                                                 | 443 ms: 1.28x slower                                                    |
| pprint_pformat             | 1.55 sec                                               | 1.99 sec: 1.28x slower                                                  |
| spectral_norm              | 108 ms                                                 | 140 ms: 1.29x slower                                                    |
| pprint_safe_repr           | 747 ms                                                 | 968 ms: 1.29x slower                                                    |
| scimark_sor                | 121 ms                                                 | 159 ms: 1.31x slower                                                    |
| mako                       | 10.7 ms                                                | 14.0 ms: 1.31x slower                                                   |
| logging_silent             | 111 ns                                                 | 146 ns: 1.32x slower                                                    |
| django_template            | 33.5 ms                                                | 44.5 ms: 1.33x slower                                                   |
| regex_compile              | 141 ms                                                 | 190 ms: 1.34x slower                                                    |
| genshi_xml                 | 53.4 ms                                                | 72.9 ms: 1.36x slower                                                   |
| telco                      | 6.86 ms                                                | 9.60 ms: 1.40x slower                                                   |
| hexiom                     | 6.89 ms                                                | 9.66 ms: 1.40x slower                                                   |
| pyflate                    | 434 ms                                                 | 609 ms: 1.40x slower                                                    |
| genshi_text                | 22.5 ms                                                | 32.0 ms: 1.42x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 167 ms: 1.43x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                            |

Benchmark hidden because not significant (4): djangocms, json, bench_mp_pool, pathlib
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.04x
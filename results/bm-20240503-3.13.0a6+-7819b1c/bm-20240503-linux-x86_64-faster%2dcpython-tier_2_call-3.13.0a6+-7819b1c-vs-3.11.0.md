# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 7819b1c
- commit date: 2024-05-03
- overall geometric mean: 1.06x faster
- HPT reliability: 98.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                    |
| chameleon      | 6.70 ms                                                | 6.96 ms: 1.04x slower                                                   |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                  |
| html5lib       | 64.8 ms                                                | 67.0 ms: 1.03x slower                                                   |
| tornado_http   | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 353 ms: 1.49x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 951 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 85.7 ms: 1.12x faster                                                   |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                    |
| regex_effbot   | 3.51 ms                                                | 3.84 ms: 1.09x slower                                                   |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                                    |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.25x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 216 us: 1.12x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                  |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                   |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                    |
| unpickle_list        | 5.21 us                                                | 5.14 us: 1.02x faster                                                   |
| pickle_dict          | 34.6 us                                                | 35.7 us: 1.03x slower                                                   |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                   |
| unpickle             | 13.8 us                                                | 15.2 us: 1.09x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.32 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.9 ms: 1.05x faster                                                   |
| mako            | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                   |
| genshi_text     | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                   |
| django_template | 33.5 ms                                                | 34.6 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 166 us: 3.13x faster                                                    |
| generators                 | 74.9 ms                                                | 29.0 ms: 2.58x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                  |
| async_tree_none            | 528 ms                                                 | 353 ms: 1.49x faster                                                    |
| pylint                     | 476 ms                                                 | 320 ms: 1.49x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                    |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 951 ms: 1.36x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                    |
| deltablue                  | 3.92 ms                                                | 3.24 ms: 1.21x faster                                                   |
| chaos                      | 71.9 ms                                                | 60.6 ms: 1.19x faster                                                   |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                   |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                    |
| richards_super             | 61.9 ms                                                | 54.2 ms: 1.14x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.12 ms: 1.13x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 216 us: 1.12x faster                                                    |
| nbody                      | 96.0 ms                                                | 85.7 ms: 1.12x faster                                                   |
| nqueens                    | 87.9 ms                                                | 79.3 ms: 1.11x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                   |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.61 ms: 1.08x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                    |
| logging_simple             | 6.22 us                                                | 5.76 us: 1.08x faster                                                   |
| logging_format             | 6.81 us                                                | 6.34 us: 1.07x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.74 ms: 1.07x faster                                                   |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.07x faster                                                    |
| pathlib                    | 18.5 ms                                                | 17.4 ms: 1.06x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                  |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                   |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                   |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                    |
| genshi_xml                 | 53.4 ms                                                | 50.9 ms: 1.05x faster                                                   |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                    |
| scimark_monte_carlo        | 70.7 ms                                                | 67.6 ms: 1.05x faster                                                   |
| tornado_http               | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                   |
| djangocms                  | 33.5 us                                                | 32.2 us: 1.04x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                    |
| richards                   | 49.8 ms                                                | 47.9 ms: 1.04x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 74.1 ms: 1.03x faster                                                   |
| fannkuch                   | 405 ms                                                 | 392 ms: 1.03x faster                                                    |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                                    |
| sympy_expand               | 484 ms                                                 | 471 ms: 1.03x faster                                                    |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                    |
| deepcopy                   | 365 us                                                 | 359 us: 1.02x faster                                                    |
| unpickle_list              | 5.21 us                                                | 5.14 us: 1.02x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 54.8 ms: 1.01x faster                                                   |
| mdp                        | 2.77 sec                                               | 2.75 sec: 1.01x faster                                                  |
| scimark_lu                 | 116 ms                                                 | 116 ms: 1.01x faster                                                    |
| bench_thread_pool          | 834 us                                                 | 831 us: 1.00x faster                                                    |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                   |
| pprint_safe_repr           | 747 ms                                                 | 753 ms: 1.01x slower                                                    |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                                   |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                  |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                    |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.15 ms: 1.02x slower                                                   |
| genshi_text                | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                   |
| django_template            | 33.5 ms                                                | 34.6 ms: 1.03x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.7 us: 1.03x slower                                                   |
| html5lib                   | 64.8 ms                                                | 67.0 ms: 1.03x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 67.0 ms: 1.04x slower                                                   |
| chameleon                  | 6.70 ms                                                | 6.96 ms: 1.04x slower                                                   |
| thrift                     | 784 us                                                 | 826 us: 1.05x slower                                                    |
| aiohttp                    | 1.12 ms                                                | 1.18 ms: 1.05x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.28 ms: 1.07x slower                                                   |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                   |
| scimark_fft                | 345 ms                                                 | 371 ms: 1.07x slower                                                    |
| xml_etree_process          | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                   |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.08x slower                                                    |
| mypy2                      | 686 ms                                                 | 738 ms: 1.08x slower                                                    |
| xml_etree_generate         | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                   |
| scimark_sor                | 121 ms                                                 | 132 ms: 1.09x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.84 ms: 1.09x slower                                                   |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.09x slower                                                   |
| pyflate                    | 434 ms                                                 | 477 ms: 1.10x slower                                                    |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.92 us: 1.14x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.32 us: 1.16x slower                                                   |
| coverage                   | 78.8 ms                                                | 92.5 ms: 1.17x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                   |
| async_generators           | 374 ms                                                 | 442 ms: 1.18x slower                                                    |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                   |
| flaskblogging              | 7.28 ms                                                | 8.93 ms: 1.23x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| telco                      | 6.86 ms                                                | 8.55 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (3): json, float, dask
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.93% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
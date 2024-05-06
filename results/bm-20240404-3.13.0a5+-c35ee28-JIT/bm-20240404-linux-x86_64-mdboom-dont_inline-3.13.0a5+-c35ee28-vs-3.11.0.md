# Results vs. 3.11.0

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.05x faster
- HPT reliability: 62.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                          |
| chameleon      | 6.70 ms                                                | 6.86 ms: 1.02x slower                                         |
| docutils       | 2.66 sec                                               | 2.92 sec: 1.10x slower                                        |
| html5lib       | 64.8 ms                                                | 67.7 ms: 1.04x slower                                         |
| tornado_http   | 98.1 ms                                                | 96.1 ms: 1.02x faster                                         |
| Geometric mean | (ref)                                                  | 1.04x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                          |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                          |
| async_tree_memoization     | 639 ms                                                 | 458 ms: 1.39x faster                                          |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                          |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.27x faster                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                          |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 91.1 ms: 1.05x faster                                         |
| float          | 78.9 ms                                                | 76.9 ms: 1.03x faster                                         |
| pidigits       | 194 ms                                                 | 207 ms: 1.06x slower                                          |
| Geometric mean | (ref)                                                  | 1.01x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 147 ms: 1.04x slower                                          |
| regex_effbot   | 3.51 ms                                                | 3.78 ms: 1.08x slower                                         |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                         |
| regex_dna      | 205 ms                                                 | 233 ms: 1.14x slower                                          |
| Geometric mean | (ref)                                                  | 1.10x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.28x faster                                         |
| tomli_loads          | 2.30 sec                                               | 2.07 sec: 1.12x faster                                        |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.05x faster                                          |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                         |
| pickle_dict          | 34.6 us                                                | 33.9 us: 1.02x faster                                         |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.01x faster                                          |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                          |
| unpickle_pure_python | 242 us                                                 | 239 us: 1.01x faster                                          |
| unpickle_list        | 5.21 us                                                | 5.29 us: 1.01x slower                                         |
| xml_etree_process    | 56.9 ms                                                | 59.6 ms: 1.05x slower                                         |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                         |
| xml_etree_generate   | 81.1 ms                                                | 86.5 ms: 1.07x slower                                         |
| pickle_list          | 4.59 us                                                | 4.96 us: 1.08x slower                                         |
| unpickle             | 13.8 us                                                | 16.2 us: 1.17x slower                                         |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                         |
| python_startup_no_site | 6.01 ms                                                | 9.52 ms: 1.58x slower                                         |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako           | 10.7 ms                                                | 10.8 ms: 1.01x slower                                         |
| genshi_xml     | 53.4 ms                                                | 55.4 ms: 1.04x slower                                         |
| genshi_text    | 22.5 ms                                                | 24.8 ms: 1.10x slower                                         |
| Geometric mean | (ref)                                                  | 1.05x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.55x faster                                          |
| generators                 | 74.9 ms                                                | 29.5 ms: 2.54x faster                                         |
| asyncio_tcp                | 875 ms                                                 | 515 ms: 1.70x faster                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                        |
| pylint                     | 476 ms                                                 | 297 ms: 1.60x faster                                          |
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                          |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                          |
| async_tree_memoization     | 639 ms                                                 | 458 ms: 1.39x faster                                          |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                          |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                          |
| comprehensions             | 23.6 us                                                | 18.1 us: 1.30x faster                                         |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.28x faster                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.27x faster                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                          |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                         |
| richards_super             | 61.9 ms                                                | 52.7 ms: 1.17x faster                                         |
| chaos                      | 71.9 ms                                                | 61.8 ms: 1.16x faster                                         |
| deltablue                  | 3.92 ms                                                | 3.45 ms: 1.14x faster                                         |
| tomli_loads                | 2.30 sec                                               | 2.07 sec: 1.12x faster                                        |
| raytrace                   | 309 ms                                                 | 279 ms: 1.10x faster                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.08x faster                                         |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                          |
| richards                   | 49.8 ms                                                | 46.3 ms: 1.08x faster                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                         |
| gc_traversal               | 4.01 ms                                                | 3.80 ms: 1.06x faster                                         |
| nbody                      | 96.0 ms                                                | 91.1 ms: 1.05x faster                                         |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.05x faster                                          |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.84 ms: 1.04x faster                                         |
| logging_simple             | 6.22 us                                                | 5.99 us: 1.04x faster                                         |
| deepcopy_memo              | 40.2 us                                                | 38.8 us: 1.04x faster                                         |
| logging_format             | 6.81 us                                                | 6.62 us: 1.03x faster                                         |
| scimark_monte_carlo        | 70.7 ms                                                | 68.8 ms: 1.03x faster                                         |
| float                      | 78.9 ms                                                | 76.9 ms: 1.03x faster                                         |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.02x faster                                        |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                         |
| deepcopy                   | 365 us                                                 | 358 us: 1.02x faster                                          |
| tornado_http               | 98.1 ms                                                | 96.1 ms: 1.02x faster                                         |
| pickle_dict                | 34.6 us                                                | 33.9 us: 1.02x faster                                         |
| crypto_pyaes               | 76.7 ms                                                | 75.5 ms: 1.02x faster                                         |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.01x faster                                          |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                          |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                          |
| unpickle_pure_python       | 242 us                                                 | 239 us: 1.01x faster                                          |
| fannkuch                   | 405 ms                                                 | 401 ms: 1.01x faster                                          |
| sympy_str                  | 297 ms                                                 | 295 ms: 1.01x faster                                          |
| scimark_fft                | 345 ms                                                 | 343 ms: 1.01x faster                                          |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.01x slower                                         |
| unpickle_list              | 5.21 us                                                | 5.29 us: 1.01x slower                                         |
| sympy_expand               | 484 ms                                                 | 493 ms: 1.02x slower                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                         |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                         |
| mdp                        | 2.77 sec                                               | 2.83 sec: 1.02x slower                                        |
| pathlib                    | 18.5 ms                                                | 18.9 ms: 1.02x slower                                         |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                        |
| json                       | 5.24 ms                                                | 5.36 ms: 1.02x slower                                         |
| dask                       | 365 ms                                                 | 374 ms: 1.02x slower                                          |
| chameleon                  | 6.70 ms                                                | 6.86 ms: 1.02x slower                                         |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.03x slower                                          |
| bench_thread_pool          | 834 us                                                 | 858 us: 1.03x slower                                          |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                          |
| hexiom                     | 6.89 ms                                                | 7.10 ms: 1.03x slower                                         |
| genshi_xml                 | 53.4 ms                                                | 55.4 ms: 1.04x slower                                         |
| go                         | 149 ms                                                 | 154 ms: 1.04x slower                                          |
| regex_compile              | 141 ms                                                 | 147 ms: 1.04x slower                                          |
| sqlglot_optimize           | 55.3 ms                                                | 57.7 ms: 1.04x slower                                         |
| html5lib                   | 64.8 ms                                                | 67.7 ms: 1.04x slower                                         |
| xml_etree_process          | 56.9 ms                                                | 59.6 ms: 1.05x slower                                         |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                          |
| nqueens                    | 87.9 ms                                                | 92.2 ms: 1.05x slower                                         |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                          |
| pidigits                   | 194 ms                                                 | 207 ms: 1.06x slower                                          |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                         |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.07x slower                                          |
| xml_etree_generate         | 81.1 ms                                                | 86.5 ms: 1.07x slower                                         |
| regex_effbot               | 3.51 ms                                                | 3.78 ms: 1.08x slower                                         |
| pickle_list                | 4.59 us                                                | 4.96 us: 1.08x slower                                         |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                         |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                         |
| dulwich_log                | 64.6 ms                                                | 70.9 ms: 1.10x slower                                         |
| docutils                   | 2.66 sec                                               | 2.92 sec: 1.10x slower                                        |
| pyflate                    | 434 ms                                                 | 476 ms: 1.10x slower                                          |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                         |
| sqlite_synth               | 2.57 us                                                | 2.88 us: 1.12x slower                                         |
| scimark_sor                | 121 ms                                                 | 136 ms: 1.12x slower                                          |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                         |
| regex_dna                  | 205 ms                                                 | 233 ms: 1.14x slower                                          |
| scimark_lu                 | 116 ms                                                 | 133 ms: 1.15x slower                                          |
| mypy2                      | 686 ms                                                 | 788 ms: 1.15x slower                                          |
| unpickle                   | 13.8 us                                                | 16.2 us: 1.17x slower                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                         |
| async_generators           | 374 ms                                                 | 461 ms: 1.23x slower                                          |
| telco                      | 6.86 ms                                                | 8.49 ms: 1.24x slower                                         |
| coverage                   | 78.8 ms                                                | 100 ms: 1.27x slower                                          |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                         |
| python_startup_no_site     | 6.01 ms                                                | 9.52 ms: 1.58x slower                                         |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                  |

Benchmark hidden because not significant (3): pprint_safe_repr, bench_mp_pool, sqlglot_normalize
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 62.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
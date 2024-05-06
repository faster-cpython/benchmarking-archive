# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 1e4a4c4
- commit date: 2024-04-19
- overall geometric mean: 1.04x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 301 ms: 1.14x slower                                   |
| chameleon      | 6.70 ms                                                | 7.65 ms: 1.14x slower                                  |
| docutils       | 2.66 sec                                               | 3.08 sec: 1.16x slower                                 |
| html5lib       | 64.8 ms                                                | 72.5 ms: 1.12x slower                                  |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.05x slower                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                   |
| async_tree_none_tg         | 491 ms                                                 | 356 ms: 1.38x faster                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 466 ms: 1.34x faster                                   |
| async_tree_io_tg           | 1.29 sec                                               | 973 ms: 1.33x faster                                   |
| async_tree_io              | 1.29 sec                                               | 984 ms: 1.31x faster                                   |
| async_tree_memoization     | 639 ms                                                 | 501 ms: 1.27x faster                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 627 ms: 1.21x faster                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 636 ms: 1.18x faster                                   |
| Geometric mean             | (ref)                                                  | 1.30x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 208 ms: 1.07x slower                                   |
| float          | 78.9 ms                                                | 89.3 ms: 1.13x slower                                  |
| nbody          | 96.0 ms                                                | 119 ms: 1.24x slower                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.88 ms: 1.11x slower                                  |
| regex_v8       | 22.9 ms                                                | 26.2 ms: 1.14x slower                                  |
| regex_dna      | 205 ms                                                 | 234 ms: 1.14x slower                                   |
| regex_compile  | 141 ms                                                 | 177 ms: 1.26x slower                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                  |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| json_loads           | 29.2 us                                                | 28.0 us: 1.04x faster                                  |
| pickle_pure_python   | 320 us                                                 | 311 us: 1.03x faster                                   |
| xml_etree_iterparse  | 108 ms                                                 | 110 ms: 1.02x slower                                   |
| unpickle_list        | 5.21 us                                                | 5.49 us: 1.05x slower                                  |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                  |
| tomli_loads          | 2.30 sec                                               | 2.51 sec: 1.09x slower                                 |
| pickle_list          | 4.59 us                                                | 5.07 us: 1.11x slower                                  |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                  |
| xml_etree_process    | 56.9 ms                                                | 63.8 ms: 1.12x slower                                  |
| xml_etree_generate   | 81.1 ms                                                | 93.5 ms: 1.15x slower                                  |
| unpickle_pure_python | 242 us                                                 | 282 us: 1.17x slower                                   |
| Geometric mean       | (ref)                                                  | 1.03x slower                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.13 ms: 1.19x slower                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 59.0 ms: 1.10x slower                                  |
| genshi_text     | 22.5 ms                                                | 25.7 ms: 1.14x slower                                  |
| django_template | 33.5 ms                                                | 39.5 ms: 1.18x slower                                  |
| mako            | 10.7 ms                                                | 13.6 ms: 1.28x slower                                  |
| Geometric mean  | (ref)                                                  | 1.17x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 119 us: 4.35x faster                                   |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                  |
| asyncio_tcp                | 875 ms                                                 | 522 ms: 1.68x faster                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                 |
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                   |
| pylint                     | 476 ms                                                 | 342 ms: 1.39x faster                                   |
| async_tree_none_tg         | 491 ms                                                 | 356 ms: 1.38x faster                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 466 ms: 1.34x faster                                   |
| async_tree_io_tg           | 1.29 sec                                               | 973 ms: 1.33x faster                                   |
| async_tree_io              | 1.29 sec                                               | 984 ms: 1.31x faster                                   |
| async_tree_memoization     | 639 ms                                                 | 501 ms: 1.27x faster                                   |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 627 ms: 1.21x faster                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 636 ms: 1.18x faster                                   |
| coroutines                 | 27.0 ms                                                | 23.3 ms: 1.16x faster                                  |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| comprehensions             | 23.6 us                                                | 22.4 us: 1.05x faster                                  |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                   |
| json_loads                 | 29.2 us                                                | 28.0 us: 1.04x faster                                  |
| pickle_pure_python         | 320 us                                                 | 311 us: 1.03x faster                                   |
| djangocms                  | 33.5 us                                                | 32.7 us: 1.03x faster                                  |
| gc_traversal               | 4.01 ms                                                | 3.94 ms: 1.02x faster                                  |
| pathlib                    | 18.5 ms                                                | 18.2 ms: 1.02x faster                                  |
| json                       | 5.24 ms                                                | 5.19 ms: 1.01x faster                                  |
| logging_simple             | 6.22 us                                                | 6.32 us: 1.02x slower                                  |
| xml_etree_iterparse        | 108 ms                                                 | 110 ms: 1.02x slower                                   |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.30 us: 1.03x slower                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.80 ms: 1.03x slower                                  |
| logging_format             | 6.81 us                                                | 7.01 us: 1.03x slower                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.48 ms: 1.03x slower                                  |
| deltablue                  | 3.92 ms                                                | 4.06 ms: 1.03x slower                                  |
| deepcopy                   | 365 us                                                 | 378 us: 1.04x slower                                   |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                   |
| raytrace                   | 309 ms                                                 | 323 ms: 1.05x slower                                   |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.05x slower                                   |
| mdp                        | 2.77 sec                                               | 2.91 sec: 1.05x slower                                 |
| unpickle_list              | 5.21 us                                                | 5.49 us: 1.05x slower                                  |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.05x slower                                   |
| bench_thread_pool          | 834 us                                                 | 882 us: 1.06x slower                                   |
| thrift                     | 784 us                                                 | 838 us: 1.07x slower                                   |
| pidigits                   | 194 ms                                                 | 208 ms: 1.07x slower                                   |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                  |
| sympy_str                  | 297 ms                                                 | 322 ms: 1.08x slower                                   |
| sympy_integrate            | 21.5 ms                                                | 23.2 ms: 1.08x slower                                  |
| tomli_loads                | 2.30 sec                                               | 2.51 sec: 1.09x slower                                 |
| sqlglot_normalize          | 113 ms                                                 | 123 ms: 1.09x slower                                   |
| meteor_contest             | 109 ms                                                 | 119 ms: 1.09x slower                                   |
| chaos                      | 71.9 ms                                                | 78.7 ms: 1.10x slower                                  |
| sympy_expand               | 484 ms                                                 | 533 ms: 1.10x slower                                   |
| genshi_xml                 | 53.4 ms                                                | 59.0 ms: 1.10x slower                                  |
| gunicorn                   | 1.20 ms                                                | 1.32 ms: 1.10x slower                                  |
| richards                   | 49.8 ms                                                | 55.0 ms: 1.10x slower                                  |
| aiohttp                    | 1.12 ms                                                | 1.23 ms: 1.10x slower                                  |
| pickle_list                | 4.59 us                                                | 5.07 us: 1.11x slower                                  |
| regex_effbot               | 3.51 ms                                                | 3.88 ms: 1.11x slower                                  |
| pycparser                  | 1.19 sec                                               | 1.31 sec: 1.11x slower                                 |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                  |
| deepcopy_memo              | 40.2 us                                                | 44.8 us: 1.11x slower                                  |
| html5lib                   | 64.8 ms                                                | 72.5 ms: 1.12x slower                                  |
| xml_etree_process          | 56.9 ms                                                | 63.8 ms: 1.12x slower                                  |
| float                      | 78.9 ms                                                | 89.3 ms: 1.13x slower                                  |
| 2to3                       | 264 ms                                                 | 301 ms: 1.14x slower                                   |
| sqlglot_optimize           | 55.3 ms                                                | 63.1 ms: 1.14x slower                                  |
| chameleon                  | 6.70 ms                                                | 7.65 ms: 1.14x slower                                  |
| dulwich_log                | 64.6 ms                                                | 73.8 ms: 1.14x slower                                  |
| genshi_text                | 22.5 ms                                                | 25.7 ms: 1.14x slower                                  |
| regex_v8                   | 22.9 ms                                                | 26.2 ms: 1.14x slower                                  |
| regex_dna                  | 205 ms                                                 | 234 ms: 1.14x slower                                   |
| xml_etree_generate         | 81.1 ms                                                | 93.5 ms: 1.15x slower                                  |
| docutils                   | 2.66 sec                                               | 3.08 sec: 1.16x slower                                 |
| unpickle_pure_python       | 242 us                                                 | 282 us: 1.17x slower                                   |
| mypy2                      | 686 ms                                                 | 803 ms: 1.17x slower                                   |
| django_template            | 33.5 ms                                                | 39.5 ms: 1.18x slower                                  |
| sqlite_synth               | 2.57 us                                                | 3.04 us: 1.18x slower                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.13 ms: 1.19x slower                                  |
| crypto_pyaes               | 76.7 ms                                                | 91.7 ms: 1.20x slower                                  |
| fannkuch                   | 405 ms                                                 | 489 ms: 1.21x slower                                   |
| go                         | 149 ms                                                 | 182 ms: 1.23x slower                                   |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                  |
| scimark_sor                | 121 ms                                                 | 150 ms: 1.24x slower                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.24x slower                                  |
| nbody                      | 96.0 ms                                                | 119 ms: 1.24x slower                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.28 ms: 1.25x slower                                  |
| nqueens                    | 87.9 ms                                                | 110 ms: 1.25x slower                                   |
| regex_compile              | 141 ms                                                 | 177 ms: 1.26x slower                                   |
| coverage                   | 78.8 ms                                                | 99.4 ms: 1.26x slower                                  |
| pprint_safe_repr           | 747 ms                                                 | 947 ms: 1.27x slower                                   |
| pprint_pformat             | 1.55 sec                                               | 1.97 sec: 1.27x slower                                 |
| async_generators           | 374 ms                                                 | 476 ms: 1.27x slower                                   |
| mako                       | 10.7 ms                                                | 13.6 ms: 1.28x slower                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 91.3 ms: 1.29x slower                                  |
| scimark_fft                | 345 ms                                                 | 461 ms: 1.34x slower                                   |
| telco                      | 6.86 ms                                                | 9.19 ms: 1.34x slower                                  |
| spectral_norm              | 108 ms                                                 | 147 ms: 1.36x slower                                   |
| pyflate                    | 434 ms                                                 | 589 ms: 1.36x slower                                   |
| hexiom                     | 6.89 ms                                                | 9.41 ms: 1.37x slower                                  |
| scimark_lu                 | 116 ms                                                 | 167 ms: 1.44x slower                                   |
| Geometric mean             | (ref)                                                  | 1.04x slower                                           |

Benchmark hidden because not significant (3): bench_mp_pool, pickle_dict, richards_super
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.03x
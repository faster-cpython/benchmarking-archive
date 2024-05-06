# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_refactor
- machine: linux-x86_64
- commit hash: 8ca0f58
- commit date: 2024-04-27
- overall geometric mean: 1.06x faster
- HPT reliability: 95.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.04x slower                                                    |
| chameleon      | 6.70 ms                                                | 7.02 ms: 1.05x slower                                                   |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                  |
| html5lib       | 64.8 ms                                                | 67.5 ms: 1.04x slower                                                   |
| tornado_http   | 98.1 ms                                                | 95.6 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 930 ms: 1.38x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.38x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.9 ms: 1.07x faster                                                   |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                    |
| float          | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                    |
| regex_effbot   | 3.51 ms                                                | 3.70 ms: 1.06x slower                                                   |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                    |
| regex_v8       | 22.9 ms                                                | 26.2 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 2.04 sec: 1.13x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 153 ms: 1.07x faster                                                    |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                    |
| json_loads           | 29.2 us                                                | 28.0 us: 1.04x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 233 us: 1.04x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 104 ms: 1.03x faster                                                    |
| unpickle_list        | 5.21 us                                                | 5.20 us: 1.00x faster                                                   |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.02x slower                                                   |
| pickle               | 11.0 us                                                | 11.5 us: 1.04x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 59.6 ms: 1.05x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 87.0 ms: 1.07x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.08 us: 1.11x slower                                                   |
| unpickle             | 13.8 us                                                | 16.3 us: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.57 ms: 1.26x slower                                                   |
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.8 ms: 1.02x slower                                                   |
| django_template | 33.5 ms                                                | 35.7 ms: 1.06x slower                                                   |
| genshi_text     | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.58x faster                                                    |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 509 ms: 1.72x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                  |
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                    |
| pylint                     | 476 ms                                                 | 334 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 930 ms: 1.38x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.38x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                    |
| comprehensions             | 23.6 us                                                | 17.9 us: 1.32x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                   |
| richards_super             | 61.9 ms                                                | 49.0 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                    |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.19x faster                                                   |
| richards                   | 49.8 ms                                                | 43.1 ms: 1.15x faster                                                   |
| chaos                      | 71.9 ms                                                | 63.2 ms: 1.14x faster                                                   |
| logging_silent             | 111 ns                                                 | 98.0 ns: 1.13x faster                                                   |
| raytrace                   | 309 ms                                                 | 272 ms: 1.13x faster                                                    |
| tomli_loads                | 2.30 sec                                               | 2.04 sec: 1.13x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.62 ms: 1.08x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 153 ms: 1.07x faster                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.69 ms: 1.07x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                   |
| nbody                      | 96.0 ms                                                | 89.9 ms: 1.07x faster                                                   |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                    |
| deepcopy_memo              | 40.2 us                                                | 37.9 us: 1.06x faster                                                   |
| logging_format             | 6.81 us                                                | 6.43 us: 1.06x faster                                                   |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.05x faster                                                   |
| fannkuch                   | 405 ms                                                 | 387 ms: 1.05x faster                                                    |
| json_loads                 | 29.2 us                                                | 28.0 us: 1.04x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 73.7 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 233 us: 1.04x faster                                                    |
| deepcopy                   | 365 us                                                 | 353 us: 1.04x faster                                                    |
| xml_etree_iterparse        | 108 ms                                                 | 104 ms: 1.03x faster                                                    |
| djangocms                  | 33.5 us                                                | 32.4 us: 1.03x faster                                                   |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                    |
| scimark_fft                | 345 ms                                                 | 336 ms: 1.03x faster                                                    |
| tornado_http               | 98.1 ms                                                | 95.6 ms: 1.03x faster                                                   |
| json                       | 5.24 ms                                                | 5.12 ms: 1.02x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 69.1 ms: 1.02x faster                                                   |
| float                      | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                   |
| sympy_str                  | 297 ms                                                 | 291 ms: 1.02x faster                                                    |
| sympy_sum                  | 169 ms                                                 | 165 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 3.22 us                                                | 3.17 us: 1.01x faster                                                   |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 747 ms                                                 | 740 ms: 1.01x faster                                                    |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                    |
| unpickle_list              | 5.21 us                                                | 5.20 us: 1.00x faster                                                   |
| sympy_expand               | 484 ms                                                 | 489 ms: 1.01x slower                                                    |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                    |
| sympy_integrate            | 21.5 ms                                                | 21.8 ms: 1.01x slower                                                   |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.02x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.02x slower                                                   |
| dask                       | 365 ms                                                 | 373 ms: 1.02x slower                                                    |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 852 us: 1.02x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 56.7 ms: 1.03x slower                                                   |
| go                         | 149 ms                                                 | 153 ms: 1.03x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                    |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.04x slower                                                    |
| html5lib                   | 64.8 ms                                                | 67.5 ms: 1.04x slower                                                   |
| thrift                     | 784 us                                                 | 817 us: 1.04x slower                                                    |
| pickle                     | 11.0 us                                                | 11.5 us: 1.04x slower                                                   |
| 2to3                       | 264 ms                                                 | 276 ms: 1.04x slower                                                    |
| xml_etree_process          | 56.9 ms                                                | 59.6 ms: 1.05x slower                                                   |
| chameleon                  | 6.70 ms                                                | 7.02 ms: 1.05x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.70 ms: 1.06x slower                                                   |
| pyflate                    | 434 ms                                                 | 459 ms: 1.06x slower                                                    |
| django_template            | 33.5 ms                                                | 35.7 ms: 1.06x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 69.1 ms: 1.07x slower                                                   |
| scimark_sor                | 121 ms                                                 | 130 ms: 1.07x slower                                                    |
| xml_etree_generate         | 81.1 ms                                                | 87.0 ms: 1.07x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.08x slower                                                   |
| genshi_text                | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                   |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.08x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                  |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.08 us: 1.11x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 130 ms: 1.12x slower                                                    |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                                   |
| mypy2                      | 686 ms                                                 | 780 ms: 1.14x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 26.2 ms: 1.15x slower                                                   |
| unpickle                   | 13.8 us                                                | 16.3 us: 1.17x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                   |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                    |
| telco                      | 6.86 ms                                                | 8.56 ms: 1.25x slower                                                   |
| coverage                   | 78.8 ms                                                | 98.7 ms: 1.25x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.57 ms: 1.26x slower                                                   |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (7): pprint_pformat, hexiom, genshi_xml, gc_traversal, mdp, bench_mp_pool, nqueens
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 95.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
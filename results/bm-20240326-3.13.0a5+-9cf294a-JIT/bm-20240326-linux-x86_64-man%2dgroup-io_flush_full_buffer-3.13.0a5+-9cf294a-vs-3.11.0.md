# Results vs. 3.11.0

- fork: man-group
- ref: io_flush_full_buffer
- machine: linux-x86_64
- commit hash: 9cf294a
- commit date: 2024-03-26
- overall geometric mean: 1.04x faster
- HPT reliability: 65.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.05x slower                                                        |
| chameleon      | 6.70 ms                                                | 6.93 ms: 1.03x slower                                                       |
| docutils       | 2.66 sec                                               | 2.87 sec: 1.08x slower                                                      |
| html5lib       | 64.8 ms                                                | 66.0 ms: 1.02x slower                                                       |
| tornado_http   | 98.1 ms                                                | 96.4 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                        |
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 919 ms: 1.41x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 919 ms: 1.40x faster                                                        |
| async_tree_none_tg         | 491 ms                                                 | 351 ms: 1.40x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 594 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                        |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 189 ms: 1.02x faster                                                        |
| nbody          | 96.0 ms                                                | 93.8 ms: 1.02x faster                                                       |
| float          | 78.9 ms                                                | 77.5 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 146 ms: 1.03x slower                                                        |
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                       |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                                        |
| regex_v8       | 22.9 ms                                                | 26.2 ms: 1.14x slower                                                       |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps          | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                       |
| tomli_loads         | 2.30 sec                                               | 2.09 sec: 1.10x faster                                                      |
| pickle_pure_python  | 320 us                                                 | 309 us: 1.04x faster                                                        |
| pickle_dict         | 34.6 us                                                | 33.5 us: 1.03x faster                                                       |
| json_loads          | 29.2 us                                                | 28.3 us: 1.03x faster                                                       |
| xml_etree_parse     | 164 ms                                                 | 160 ms: 1.02x faster                                                        |
| unpickle_list       | 5.21 us                                                | 5.11 us: 1.02x faster                                                       |
| xml_etree_iterparse | 108 ms                                                 | 107 ms: 1.01x faster                                                        |
| xml_etree_generate  | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                       |
| xml_etree_process   | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                       |
| pickle              | 11.0 us                                                | 11.8 us: 1.07x slower                                                       |
| pickle_list         | 4.59 us                                                | 5.02 us: 1.09x slower                                                       |
| unpickle            | 13.8 us                                                | 15.2 us: 1.10x slower                                                       |
| Geometric mean      | (ref)                                                  | 1.01x faster                                                                |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                       |
| python_startup_no_site | 6.01 ms                                                | 9.50 ms: 1.58x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                       |
| genshi_xml      | 53.4 ms                                                | 56.3 ms: 1.05x slower                                                       |
| django_template | 33.5 ms                                                | 36.3 ms: 1.08x slower                                                       |
| genshi_text     | 22.5 ms                                                | 25.3 ms: 1.13x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.58x faster                                                        |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.50x faster                                                       |
| asyncio_tcp                | 875 ms                                                 | 504 ms: 1.74x faster                                                        |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                        |
| pylint                     | 476 ms                                                 | 337 ms: 1.41x faster                                                        |
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 919 ms: 1.41x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 919 ms: 1.40x faster                                                        |
| async_tree_none_tg         | 491 ms                                                 | 351 ms: 1.40x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                        |
| comprehensions             | 23.6 us                                                | 18.2 us: 1.29x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 594 ms: 1.26x faster                                                        |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                        |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                       |
| richards_super             | 61.9 ms                                                | 52.3 ms: 1.18x faster                                                       |
| deltablue                  | 3.92 ms                                                | 3.47 ms: 1.13x faster                                                       |
| chaos                      | 71.9 ms                                                | 64.6 ms: 1.11x faster                                                       |
| tomli_loads                | 2.30 sec                                               | 2.09 sec: 1.10x faster                                                      |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                        |
| djangocms                  | 33.5 us                                                | 31.2 us: 1.07x faster                                                       |
| richards                   | 49.8 ms                                                | 46.4 ms: 1.07x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.34 ms: 1.07x faster                                                       |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.06x faster                                                       |
| raytrace                   | 309 ms                                                 | 293 ms: 1.05x faster                                                        |
| mdp                        | 2.77 sec                                               | 2.65 sec: 1.05x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 309 us: 1.04x faster                                                        |
| logging_simple             | 6.22 us                                                | 6.00 us: 1.04x faster                                                       |
| pickle_dict                | 34.6 us                                                | 33.5 us: 1.03x faster                                                       |
| json_loads                 | 29.2 us                                                | 28.3 us: 1.03x faster                                                       |
| logging_format             | 6.81 us                                                | 6.62 us: 1.03x faster                                                       |
| crypto_pyaes               | 76.7 ms                                                | 74.6 ms: 1.03x faster                                                       |
| sympy_sum                  | 169 ms                                                 | 165 ms: 1.02x faster                                                        |
| pidigits                   | 194 ms                                                 | 189 ms: 1.02x faster                                                        |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                        |
| nbody                      | 96.0 ms                                                | 93.8 ms: 1.02x faster                                                       |
| fannkuch                   | 405 ms                                                 | 397 ms: 1.02x faster                                                        |
| unpickle_list              | 5.21 us                                                | 5.11 us: 1.02x faster                                                       |
| float                      | 78.9 ms                                                | 77.5 ms: 1.02x faster                                                       |
| sympy_str                  | 297 ms                                                 | 292 ms: 1.02x faster                                                        |
| gc_traversal               | 4.01 ms                                                | 3.94 ms: 1.02x faster                                                       |
| tornado_http               | 98.1 ms                                                | 96.4 ms: 1.02x faster                                                       |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.01x faster                                                      |
| deepcopy_reduce            | 3.22 us                                                | 3.17 us: 1.01x faster                                                       |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                        |
| deepcopy_memo              | 40.2 us                                                | 39.8 us: 1.01x faster                                                       |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                       |
| scimark_fft                | 345 ms                                                 | 347 ms: 1.01x slower                                                        |
| json                       | 5.24 ms                                                | 5.29 ms: 1.01x slower                                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 71.4 ms: 1.01x slower                                                       |
| sympy_integrate            | 21.5 ms                                                | 21.8 ms: 1.01x slower                                                       |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.01x slower                                                        |
| html5lib                   | 64.8 ms                                                | 66.0 ms: 1.02x slower                                                       |
| sympy_expand               | 484 ms                                                 | 494 ms: 1.02x slower                                                        |
| pathlib                    | 18.5 ms                                                | 18.9 ms: 1.02x slower                                                       |
| dask                       | 365 ms                                                 | 374 ms: 1.03x slower                                                        |
| bench_thread_pool          | 834 us                                                 | 858 us: 1.03x slower                                                        |
| nqueens                    | 87.9 ms                                                | 90.4 ms: 1.03x slower                                                       |
| regex_compile              | 141 ms                                                 | 146 ms: 1.03x slower                                                        |
| chameleon                  | 6.70 ms                                                | 6.93 ms: 1.03x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                                        |
| pycparser                  | 1.19 sec                                               | 1.23 sec: 1.04x slower                                                      |
| thrift                     | 784 us                                                 | 818 us: 1.04x slower                                                        |
| hexiom                     | 6.89 ms                                                | 7.20 ms: 1.05x slower                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 57.9 ms: 1.05x slower                                                       |
| go                         | 149 ms                                                 | 156 ms: 1.05x slower                                                        |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 56.3 ms: 1.05x slower                                                       |
| 2to3                       | 264 ms                                                 | 278 ms: 1.05x slower                                                        |
| spectral_norm              | 108 ms                                                 | 114 ms: 1.05x slower                                                        |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                       |
| xml_etree_process          | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                       |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                       |
| docutils                   | 2.66 sec                                               | 2.87 sec: 1.08x slower                                                      |
| django_template            | 33.5 ms                                                | 36.3 ms: 1.08x slower                                                       |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                                       |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                       |
| dulwich_log                | 64.6 ms                                                | 70.6 ms: 1.09x slower                                                       |
| pickle_list                | 4.59 us                                                | 5.02 us: 1.09x slower                                                       |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                       |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.10x slower                                                        |
| pyflate                    | 434 ms                                                 | 480 ms: 1.11x slower                                                        |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.12x slower                                                       |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                                        |
| genshi_text                | 22.5 ms                                                | 25.3 ms: 1.13x slower                                                       |
| regex_v8                   | 22.9 ms                                                | 26.2 ms: 1.14x slower                                                       |
| scimark_lu                 | 116 ms                                                 | 133 ms: 1.15x slower                                                        |
| mypy2                      | 686 ms                                                 | 787 ms: 1.15x slower                                                        |
| create_gc_cycles           | 1.43 ms                                                | 1.69 ms: 1.18x slower                                                       |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                        |
| telco                      | 6.86 ms                                                | 8.59 ms: 1.25x slower                                                       |
| coverage                   | 78.8 ms                                                | 98.7 ms: 1.25x slower                                                       |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                       |
| python_startup_no_site     | 6.01 ms                                                | 9.50 ms: 1.58x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                |

Benchmark hidden because not significant (6): deepcopy, sqlglot_normalize, bench_mp_pool, pprint_safe_repr, scimark_sparse_mat_mult, unpickle_pure_python
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 65.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
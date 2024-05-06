# Results vs. 3.11.0

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.05x faster
- HPT reliability: 63.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| chameleon      | 6.70 ms                                                | 6.86 ms: 1.02x slower                                                  |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                 |
| tornado_http   | 98.1 ms                                                | 96.1 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 454 ms: 1.41x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 91.7 ms: 1.05x faster                                                  |
| float          | 78.9 ms                                                | 76.2 ms: 1.04x faster                                                  |
| pidigits       | 194 ms                                                 | 202 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.60 ms: 1.03x slower                                                  |
| regex_compile  | 141 ms                                                 | 146 ms: 1.03x slower                                                   |
| regex_dna      | 205 ms                                                 | 220 ms: 1.08x slower                                                   |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                   |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 236 us: 1.02x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.0 us: 1.02x faster                                                  |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| xml_etree_process    | 56.9 ms                                                | 59.7 ms: 1.05x slower                                                  |
| unpickle             | 13.8 us                                                | 14.8 us: 1.07x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                  |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.02 us: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| python_startup_no_site | 6.01 ms                                                | 9.49 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                  |
| genshi_xml     | 53.4 ms                                                | 55.0 ms: 1.03x slower                                                  |
| genshi_text    | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 111 us: 4.68x faster                                                   |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 520 ms: 1.68x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                 |
| pylint                     | 476 ms                                                 | 298 ms: 1.60x faster                                                   |
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 454 ms: 1.41x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                   |
| comprehensions             | 23.6 us                                                | 17.9 us: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.2 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                   |
| richards_super             | 61.9 ms                                                | 52.2 ms: 1.19x faster                                                  |
| chaos                      | 71.9 ms                                                | 62.1 ms: 1.16x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.42 ms: 1.15x faster                                                  |
| logging_silent             | 111 ns                                                 | 97.9 ns: 1.13x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| raytrace                   | 309 ms                                                 | 280 ms: 1.10x faster                                                   |
| richards                   | 49.8 ms                                                | 45.9 ms: 1.08x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.79 ms: 1.06x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.63 sec: 1.05x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                   |
| nbody                      | 96.0 ms                                                | 91.7 ms: 1.05x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.98 us: 1.04x faster                                                  |
| float                      | 78.9 ms                                                | 76.2 ms: 1.04x faster                                                  |
| logging_format             | 6.81 us                                                | 6.61 us: 1.03x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                 |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.03x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 74.9 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 236 us: 1.02x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 69.3 ms: 1.02x faster                                                  |
| tornado_http               | 98.1 ms                                                | 96.1 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 733 ms: 1.02x faster                                                   |
| pickle_dict                | 34.6 us                                                | 34.0 us: 1.02x faster                                                  |
| fannkuch                   | 405 ms                                                 | 398 ms: 1.02x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| sympy_str                  | 297 ms                                                 | 294 ms: 1.01x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                   |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                   |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                   |
| sympy_expand               | 484 ms                                                 | 494 ms: 1.02x slower                                                   |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                  |
| chameleon                  | 6.70 ms                                                | 6.86 ms: 1.02x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.60 ms: 1.03x slower                                                  |
| hexiom                     | 6.89 ms                                                | 7.08 ms: 1.03x slower                                                  |
| dask                       | 365 ms                                                 | 376 ms: 1.03x slower                                                   |
| bench_thread_pool          | 834 us                                                 | 859 us: 1.03x slower                                                   |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                                  |
| genshi_xml                 | 53.4 ms                                                | 55.0 ms: 1.03x slower                                                  |
| go                         | 149 ms                                                 | 153 ms: 1.03x slower                                                   |
| regex_compile              | 141 ms                                                 | 146 ms: 1.03x slower                                                   |
| json                       | 5.24 ms                                                | 5.44 ms: 1.04x slower                                                  |
| pidigits                   | 194 ms                                                 | 202 ms: 1.04x slower                                                   |
| nqueens                    | 87.9 ms                                                | 91.4 ms: 1.04x slower                                                  |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 58.0 ms: 1.05x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 59.7 ms: 1.05x slower                                                  |
| thrift                     | 784 us                                                 | 826 us: 1.05x slower                                                   |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.06x slower                                                   |
| unpickle                   | 13.8 us                                                | 14.8 us: 1.07x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                  |
| regex_dna                  | 205 ms                                                 | 220 ms: 1.08x slower                                                   |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                  |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                  |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.02 us: 1.09x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 71.2 ms: 1.10x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                                  |
| scimark_sor                | 121 ms                                                 | 135 ms: 1.12x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 132 ms: 1.14x slower                                                   |
| mypy2                      | 686 ms                                                 | 786 ms: 1.15x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                  |
| async_generators           | 374 ms                                                 | 460 ms: 1.23x slower                                                   |
| telco                      | 6.86 ms                                                | 8.51 ms: 1.24x slower                                                  |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                  |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 9.49 ms: 1.58x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (7): unpickle_list, deepcopy, bench_mp_pool, scimark_sparse_mat_mult, scimark_fft, deepcopy_reduce, html5lib
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 63.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.08x faster
- HPT reliability: 99.89%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 267 ms: 1.01x slower                                                   |
| chameleon      | 6.70 ms                                                | 6.90 ms: 1.03x slower                                                  |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                 |
| html5lib       | 64.8 ms                                                | 67.1 ms: 1.04x slower                                                  |
| tornado_http   | 98.1 ms                                                | 94.4 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 348 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 331 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 916 ms: 1.40x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 455 ms: 1.40x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 926 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                  |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| float          | 78.9 ms                                                | 77.3 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 132 ms: 1.07x faster                                                   |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                  |
| regex_dna      | 205 ms                                                 | 224 ms: 1.09x slower                                                   |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 216 us: 1.12x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.07 us: 1.03x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                   |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                  |
| pickle_dict          | 34.6 us                                                | 35.2 us: 1.02x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 59.4 ms: 1.04x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 86.3 ms: 1.07x slower                                                  |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| unpickle             | 13.8 us                                                | 15.7 us: 1.14x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.26 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                  |
| python_startup_no_site | 6.01 ms                                                | 9.00 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 52.0 ms: 1.03x faster                                                  |
| mako           | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                  |
| genshi_text    | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.56x faster                                                   |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 507 ms: 1.73x faster                                                   |
| pylint                     | 476 ms                                                 | 278 ms: 1.71x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                 |
| async_tree_none            | 528 ms                                                 | 348 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 331 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 916 ms: 1.40x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 455 ms: 1.40x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 926 ms: 1.40x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.13 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                   |
| raytrace                   | 309 ms                                                 | 254 ms: 1.22x faster                                                   |
| chaos                      | 71.9 ms                                                | 59.4 ms: 1.21x faster                                                  |
| richards_super             | 61.9 ms                                                | 51.8 ms: 1.19x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.25 ms: 1.14x faster                                                  |
| logging_silent             | 111 ns                                                 | 98.6 ns: 1.13x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.12 ms: 1.13x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 216 us: 1.12x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.57 ms: 1.12x faster                                                  |
| nqueens                    | 87.9 ms                                                | 79.7 ms: 1.10x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 153 ms: 1.10x faster                                                   |
| richards                   | 49.8 ms                                                | 45.7 ms: 1.09x faster                                                  |
| nbody                      | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                  |
| sympy_str                  | 297 ms                                                 | 275 ms: 1.08x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 37.2 us: 1.08x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.79 us: 1.07x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                 |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                   |
| regex_compile              | 141 ms                                                 | 132 ms: 1.07x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 66.7 ms: 1.06x faster                                                  |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 72.3 ms: 1.06x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.62 sec: 1.06x faster                                                 |
| go                         | 149 ms                                                 | 141 ms: 1.05x faster                                                   |
| sympy_expand               | 484 ms                                                 | 461 ms: 1.05x faster                                                   |
| fannkuch                   | 405 ms                                                 | 386 ms: 1.05x faster                                                   |
| sqlglot_normalize          | 113 ms                                                 | 107 ms: 1.05x faster                                                   |
| deepcopy                   | 365 us                                                 | 349 us: 1.05x faster                                                   |
| scimark_lu                 | 116 ms                                                 | 112 ms: 1.04x faster                                                   |
| tornado_http               | 98.1 ms                                                | 94.4 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                 |
| unpickle_list              | 5.21 us                                                | 5.07 us: 1.03x faster                                                  |
| genshi_xml                 | 53.4 ms                                                | 52.0 ms: 1.03x faster                                                  |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 54.1 ms: 1.02x faster                                                  |
| float                      | 78.9 ms                                                | 77.3 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                   |
| pprint_safe_repr           | 747 ms                                                 | 737 ms: 1.01x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                  |
| bench_thread_pool          | 834 us                                                 | 826 us: 1.01x faster                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.19 us: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                   |
| spectral_norm              | 108 ms                                                 | 109 ms: 1.01x slower                                                   |
| 2to3                       | 264 ms                                                 | 267 ms: 1.01x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.2 us: 1.02x slower                                                  |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                   |
| chameleon                  | 6.70 ms                                                | 6.90 ms: 1.03x slower                                                  |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                  |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                   |
| html5lib                   | 64.8 ms                                                | 67.1 ms: 1.04x slower                                                  |
| scimark_fft                | 345 ms                                                 | 361 ms: 1.04x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 59.4 ms: 1.04x slower                                                  |
| scimark_sor                | 121 ms                                                 | 127 ms: 1.05x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                 |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                  |
| json                       | 5.24 ms                                                | 5.53 ms: 1.06x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 68.3 ms: 1.06x slower                                                  |
| genshi_text                | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 86.3 ms: 1.07x slower                                                  |
| mypy2                      | 686 ms                                                 | 733 ms: 1.07x slower                                                   |
| pyflate                    | 434 ms                                                 | 465 ms: 1.07x slower                                                   |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.09x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.14x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.92 us: 1.14x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.26 us: 1.15x slower                                                  |
| async_generators           | 374 ms                                                 | 438 ms: 1.17x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                  |
| telco                      | 6.86 ms                                                | 8.39 ms: 1.22x slower                                                  |
| coverage                   | 78.8 ms                                                | 96.4 ms: 1.22x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 9.00 ms: 1.50x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (4): scimark_sparse_mat_mult, pathlib, gc_traversal, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.89% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x
# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.05x faster
- HPT reliability: 50.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                  |
| docutils       | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                 |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                  |
| tornado_http   | 98.1 ms                                                | 96.9 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 606 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 91.4 ms: 1.05x faster                                                  |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| float          | 78.9 ms                                                | 78.0 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 144 ms: 1.02x slower                                                   |
| regex_effbot   | 3.51 ms                                                | 3.59 ms: 1.02x slower                                                  |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                   |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps          | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                  |
| tomli_loads         | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| pickle_pure_python  | 320 us                                                 | 307 us: 1.04x faster                                                   |
| json_loads          | 29.2 us                                                | 28.4 us: 1.03x faster                                                  |
| xml_etree_parse     | 164 ms                                                 | 160 ms: 1.03x faster                                                   |
| unpickle_list       | 5.21 us                                                | 5.15 us: 1.01x faster                                                  |
| xml_etree_iterparse | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| pickle_dict         | 34.6 us                                                | 35.1 us: 1.01x slower                                                  |
| unpickle            | 13.8 us                                                | 14.9 us: 1.08x slower                                                  |
| xml_etree_process   | 56.9 ms                                                | 61.5 ms: 1.08x slower                                                  |
| pickle              | 11.0 us                                                | 11.9 us: 1.09x slower                                                  |
| pickle_list         | 4.59 us                                                | 5.01 us: 1.09x slower                                                  |
| xml_etree_generate  | 81.1 ms                                                | 88.7 ms: 1.09x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| python_startup_no_site | 6.01 ms                                                | 9.50 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                  |
| genshi_text    | 22.5 ms                                                | 24.2 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.59x faster                                                   |
| generators                 | 74.9 ms                                                | 30.2 ms: 2.47x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 512 ms: 1.71x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                 |
| pylint                     | 476 ms                                                 | 296 ms: 1.61x faster                                                   |
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                                   |
| comprehensions             | 23.6 us                                                | 17.9 us: 1.32x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 606 ms: 1.26x faster                                                   |
| richards_super             | 61.9 ms                                                | 50.1 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                   |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.18x faster                                                  |
| chaos                      | 71.9 ms                                                | 62.6 ms: 1.15x faster                                                  |
| richards                   | 49.8 ms                                                | 44.0 ms: 1.13x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| raytrace                   | 309 ms                                                 | 278 ms: 1.11x faster                                                   |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.80 us: 1.07x faster                                                  |
| logging_format             | 6.81 us                                                | 6.40 us: 1.06x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.06x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.69 ms: 1.06x faster                                                  |
| nbody                      | 96.0 ms                                                | 91.4 ms: 1.05x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 38.4 us: 1.05x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 307 us: 1.04x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.4 us: 1.03x faster                                                  |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.91 ms: 1.02x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 69.0 ms: 1.02x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 75.6 ms: 1.01x faster                                                  |
| unpickle_list              | 5.21 us                                                | 5.15 us: 1.01x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.96 ms: 1.01x faster                                                  |
| fannkuch                   | 405 ms                                                 | 400 ms: 1.01x faster                                                   |
| tornado_http               | 98.1 ms                                                | 96.9 ms: 1.01x faster                                                  |
| float                      | 78.9 ms                                                | 78.0 ms: 1.01x faster                                                  |
| scimark_fft                | 345 ms                                                 | 342 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| deepcopy                   | 365 us                                                 | 363 us: 1.01x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.56 sec: 1.01x slower                                                 |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                  |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                   |
| json                       | 5.24 ms                                                | 5.29 ms: 1.01x slower                                                  |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.01x slower                                                  |
| mdp                        | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                 |
| regex_compile              | 141 ms                                                 | 144 ms: 1.02x slower                                                   |
| hexiom                     | 6.89 ms                                                | 7.04 ms: 1.02x slower                                                  |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.59 ms: 1.02x slower                                                  |
| sympy_expand               | 484 ms                                                 | 497 ms: 1.03x slower                                                   |
| dask                       | 365 ms                                                 | 375 ms: 1.03x slower                                                   |
| bench_thread_pool          | 834 us                                                 | 858 us: 1.03x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                   |
| sympy_integrate            | 21.5 ms                                                | 22.1 ms: 1.03x slower                                                  |
| nqueens                    | 87.9 ms                                                | 90.9 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 747 ms                                                 | 775 ms: 1.04x slower                                                   |
| go                         | 149 ms                                                 | 155 ms: 1.04x slower                                                   |
| pathlib                    | 18.5 ms                                                | 19.3 ms: 1.04x slower                                                  |
| thrift                     | 784 us                                                 | 817 us: 1.04x slower                                                   |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 58.2 ms: 1.05x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                  |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| pyflate                    | 434 ms                                                 | 464 ms: 1.07x slower                                                   |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                                   |
| genshi_text                | 22.5 ms                                                | 24.2 ms: 1.07x slower                                                  |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                   |
| unpickle                   | 13.8 us                                                | 14.9 us: 1.08x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 61.5 ms: 1.08x slower                                                  |
| pickle                     | 11.0 us                                                | 11.9 us: 1.09x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 70.6 ms: 1.09x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.01 us: 1.09x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 88.7 ms: 1.09x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                 |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.12x slower                                                  |
| scimark_lu                 | 116 ms                                                 | 134 ms: 1.15x slower                                                   |
| mypy2                      | 686 ms                                                 | 789 ms: 1.15x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                  |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                   |
| coverage                   | 78.8 ms                                                | 99.0 ms: 1.26x slower                                                  |
| telco                      | 6.86 ms                                                | 8.79 ms: 1.28x slower                                                  |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 9.50 ms: 1.58x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (7): sympy_sum, bench_mp_pool, deepcopy_reduce, sympy_str, pycparser, genshi_xml, unpickle_pure_python
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 50.42% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x
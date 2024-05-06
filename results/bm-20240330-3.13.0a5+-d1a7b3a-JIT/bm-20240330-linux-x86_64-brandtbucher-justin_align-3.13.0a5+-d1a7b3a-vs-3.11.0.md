# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.03x faster
- HPT reliability: 58.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| chameleon      | 6.70 ms                                                | 7.00 ms: 1.05x slower                                                |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                               |
| html5lib       | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                |
| tornado_http   | 98.1 ms                                                | 97.3 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 931 ms: 1.39x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 452 ms: 1.39x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 955 ms: 1.35x faster                                                 |
| async_tree_none            | 528 ms                                                 | 392 ms: 1.35x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 582 ms: 1.31x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 603 ms: 1.24x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.4 ms: 1.04x faster                                                |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                 |
| float          | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 146 ms: 1.04x slower                                                 |
| regex_effbot   | 3.51 ms                                                | 3.87 ms: 1.11x slower                                                |
| regex_v8       | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                |
| regex_dna      | 205 ms                                                 | 231 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                |
| tomli_loads          | 2.30 sec                                               | 2.10 sec: 1.09x faster                                               |
| pickle_pure_python   | 320 us                                                 | 309 us: 1.04x faster                                                 |
| unpickle_list        | 5.21 us                                                | 5.06 us: 1.03x faster                                                |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                 |
| json_loads           | 29.2 us                                                | 28.4 us: 1.03x faster                                                |
| unpickle_pure_python | 242 us                                                 | 240 us: 1.01x faster                                                 |
| pickle_dict          | 34.6 us                                                | 35.3 us: 1.02x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 89.2 ms: 1.10x slower                                                |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                                |
| pickle               | 11.0 us                                                | 12.5 us: 1.14x slower                                                |
| pickle_list          | 4.59 us                                                | 5.37 us: 1.17x slower                                                |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                |
| python_startup_no_site | 6.01 ms                                                | 9.55 ms: 1.59x slower                                                |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.8 ms: 1.02x slower                                                |
| genshi_xml      | 53.4 ms                                                | 55.3 ms: 1.03x slower                                                |
| django_template | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                |
| genshi_text     | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 115 us: 4.53x faster                                                 |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.49x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                               |
| pylint                     | 476 ms                                                 | 299 ms: 1.59x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 931 ms: 1.39x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 452 ms: 1.39x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 955 ms: 1.35x faster                                                 |
| async_tree_none            | 528 ms                                                 | 392 ms: 1.35x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 582 ms: 1.31x faster                                                 |
| comprehensions             | 23.6 us                                                | 18.3 us: 1.29x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 603 ms: 1.24x faster                                                 |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                |
| richards_super             | 61.9 ms                                                | 53.3 ms: 1.16x faster                                                |
| chaos                      | 71.9 ms                                                | 63.0 ms: 1.14x faster                                                |
| deltablue                  | 3.92 ms                                                | 3.52 ms: 1.11x faster                                                |
| tomli_loads                | 2.30 sec                                               | 2.10 sec: 1.09x faster                                               |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.35 ms: 1.06x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.05x faster                                                |
| richards                   | 49.8 ms                                                | 47.5 ms: 1.05x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.80 ms: 1.05x faster                                                |
| logging_simple             | 6.22 us                                                | 5.94 us: 1.05x faster                                                |
| raytrace                   | 309 ms                                                 | 294 ms: 1.05x faster                                                 |
| logging_format             | 6.81 us                                                | 6.53 us: 1.04x faster                                                |
| nbody                      | 96.0 ms                                                | 92.4 ms: 1.04x faster                                                |
| pickle_pure_python         | 320 us                                                 | 309 us: 1.04x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 74.4 ms: 1.03x faster                                                |
| djangocms                  | 33.5 us                                                | 32.5 us: 1.03x faster                                                |
| unpickle_list              | 5.21 us                                                | 5.06 us: 1.03x faster                                                |
| sympy_sum                  | 169 ms                                                 | 164 ms: 1.03x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                 |
| json_loads                 | 29.2 us                                                | 28.4 us: 1.03x faster                                                |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                 |
| float                      | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.02x faster                                               |
| fannkuch                   | 405 ms                                                 | 397 ms: 1.02x faster                                                 |
| sympy_str                  | 297 ms                                                 | 291 ms: 1.02x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.94 ms: 1.02x faster                                                |
| deepcopy_memo              | 40.2 us                                                | 39.6 us: 1.01x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 240 us: 1.01x faster                                                 |
| tornado_http               | 98.1 ms                                                | 97.3 ms: 1.01x faster                                                |
| scimark_fft                | 345 ms                                                 | 343 ms: 1.01x faster                                                 |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.00x faster                                                 |
| bench_mp_pool              | 24.0 ms                                                | 24.2 ms: 1.01x slower                                                |
| sympy_expand               | 484 ms                                                 | 491 ms: 1.01x slower                                                 |
| json                       | 5.24 ms                                                | 5.32 ms: 1.01x slower                                                |
| sympy_integrate            | 21.5 ms                                                | 21.8 ms: 1.02x slower                                                |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.02x slower                                                |
| mdp                        | 2.77 sec                                               | 2.83 sec: 1.02x slower                                               |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                 |
| pickle_dict                | 34.6 us                                                | 35.3 us: 1.02x slower                                                |
| bench_thread_pool          | 834 us                                                 | 856 us: 1.03x slower                                                 |
| dask                       | 365 ms                                                 | 377 ms: 1.03x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 55.3 ms: 1.03x slower                                                |
| regex_compile              | 141 ms                                                 | 146 ms: 1.04x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                                 |
| pathlib                    | 18.5 ms                                                | 19.3 ms: 1.04x slower                                                |
| pycparser                  | 1.19 sec                                               | 1.24 sec: 1.04x slower                                               |
| thrift                     | 784 us                                                 | 819 us: 1.04x slower                                                 |
| chameleon                  | 6.70 ms                                                | 7.00 ms: 1.05x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 58.0 ms: 1.05x slower                                                |
| hexiom                     | 6.89 ms                                                | 7.24 ms: 1.05x slower                                                |
| nqueens                    | 87.9 ms                                                | 92.7 ms: 1.06x slower                                                |
| html5lib                   | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| go                         | 149 ms                                                 | 157 ms: 1.06x slower                                                 |
| django_template            | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                |
| xml_etree_process          | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                |
| spectral_norm              | 108 ms                                                 | 117 ms: 1.08x slower                                                 |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                               |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                                |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.09x slower                                                 |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                |
| xml_etree_generate         | 81.1 ms                                                | 89.2 ms: 1.10x slower                                                |
| dulwich_log                | 64.6 ms                                                | 71.2 ms: 1.10x slower                                                |
| regex_effbot               | 3.51 ms                                                | 3.87 ms: 1.11x slower                                                |
| regex_v8                   | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                |
| regex_dna                  | 205 ms                                                 | 231 ms: 1.13x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.92 us: 1.13x slower                                                |
| pyflate                    | 434 ms                                                 | 493 ms: 1.14x slower                                                 |
| pickle                     | 11.0 us                                                | 12.5 us: 1.14x slower                                                |
| scimark_lu                 | 116 ms                                                 | 133 ms: 1.14x slower                                                 |
| mypy2                      | 686 ms                                                 | 789 ms: 1.15x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.37 us: 1.17x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.69 ms: 1.18x slower                                                |
| coverage                   | 78.8 ms                                                | 97.1 ms: 1.23x slower                                                |
| telco                      | 6.86 ms                                                | 8.48 ms: 1.24x slower                                                |
| async_generators           | 374 ms                                                 | 465 ms: 1.24x slower                                                 |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 9.55 ms: 1.59x slower                                                |
| unpack_sequence            | 43.5 ns                                                | 87.6 ns: 2.02x slower                                                |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (5): xml_etree_iterparse, pprint_safe_repr, deepcopy, deepcopy_reduce, scimark_monte_carlo
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 58.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
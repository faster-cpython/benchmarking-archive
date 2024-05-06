# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.05x faster
- HPT reliability: 63.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.06x slower                                                     |
| chameleon      | 6.70 ms                                                | 6.90 ms: 1.03x slower                                                    |
| docutils       | 2.66 sec                                               | 2.97 sec: 1.11x slower                                                   |
| html5lib       | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                    |
| tornado_http   | 98.1 ms                                                | 97.2 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 358 ms: 1.47x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 939 ms: 1.38x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 940 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 91.3 ms: 1.05x faster                                                    |
| float          | 78.9 ms                                                | 76.5 ms: 1.03x faster                                                    |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                  | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 145 ms: 1.03x slower                                                     |
| regex_effbot   | 3.51 ms                                                | 3.70 ms: 1.05x slower                                                    |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                                     |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|---------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 13.3 ms                                                | 10.5 ms: 1.28x faster                                                    |
| tomli_loads         | 2.30 sec                                               | 2.06 sec: 1.12x faster                                                   |
| pickle_pure_python  | 320 us                                                 | 305 us: 1.05x faster                                                     |
| json_loads          | 29.2 us                                                | 28.1 us: 1.04x faster                                                    |
| pickle_dict         | 34.6 us                                                | 34.2 us: 1.01x faster                                                    |
| xml_etree_parse     | 164 ms                                                 | 162 ms: 1.01x faster                                                     |
| xml_etree_iterparse | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| unpickle_list       | 5.21 us                                                | 5.32 us: 1.02x slower                                                    |
| xml_etree_process   | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                    |
| pickle              | 11.0 us                                                | 11.6 us: 1.06x slower                                                    |
| pickle_list         | 4.59 us                                                | 4.90 us: 1.07x slower                                                    |
| xml_etree_generate  | 81.1 ms                                                | 87.8 ms: 1.08x slower                                                    |
| unpickle            | 13.8 us                                                | 15.6 us: 1.13x slower                                                    |
| Geometric mean      | (ref)                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                    |
| python_startup_no_site | 6.01 ms                                                | 9.57 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 10.7 ms                                                | 10.6 ms: 1.00x faster                                                    |
| genshi_xml     | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                    |
| genshi_text    | 22.5 ms                                                | 24.7 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 116 us: 4.49x faster                                                     |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.49x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 527 ms: 1.66x faster                                                     |
| pylint                     | 476 ms                                                 | 304 ms: 1.57x faster                                                     |
| async_tree_none            | 528 ms                                                 | 358 ms: 1.47x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 939 ms: 1.38x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 940 ms: 1.37x faster                                                     |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.28x faster                                                    |
| comprehensions             | 23.6 us                                                | 18.6 us: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                     |
| richards_super             | 61.9 ms                                                | 49.7 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                     |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                    |
| richards                   | 49.8 ms                                                | 43.3 ms: 1.15x faster                                                    |
| chaos                      | 71.9 ms                                                | 63.1 ms: 1.14x faster                                                    |
| raytrace                   | 309 ms                                                 | 276 ms: 1.12x faster                                                     |
| tomli_loads                | 2.30 sec                                               | 2.06 sec: 1.12x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.61 ms: 1.11x faster                                                    |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                     |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                    |
| nbody                      | 96.0 ms                                                | 91.3 ms: 1.05x faster                                                    |
| logging_simple             | 6.22 us                                                | 5.93 us: 1.05x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                     |
| logging_format             | 6.81 us                                                | 6.54 us: 1.04x faster                                                    |
| mdp                        | 2.77 sec                                               | 2.66 sec: 1.04x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.1 us: 1.04x faster                                                    |
| scimark_monte_carlo        | 70.7 ms                                                | 68.2 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.86 ms: 1.03x faster                                                    |
| float                      | 78.9 ms                                                | 76.5 ms: 1.03x faster                                                    |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                     |
| deltablue                  | 3.92 ms                                                | 3.82 ms: 1.03x faster                                                    |
| deepcopy_memo              | 40.2 us                                                | 39.2 us: 1.03x faster                                                    |
| scimark_fft                | 345 ms                                                 | 337 ms: 1.02x faster                                                     |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.01x faster                                                     |
| crypto_pyaes               | 76.7 ms                                                | 76.0 ms: 1.01x faster                                                    |
| tornado_http               | 98.1 ms                                                | 97.2 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| mako                       | 10.7 ms                                                | 10.6 ms: 1.00x faster                                                    |
| go                         | 149 ms                                                 | 149 ms: 1.01x slower                                                     |
| sympy_str                  | 297 ms                                                 | 300 ms: 1.01x slower                                                     |
| deepcopy                   | 365 us                                                 | 370 us: 1.01x slower                                                     |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.02x slower                                                     |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                                    |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                                     |
| unpickle_list              | 5.21 us                                                | 5.32 us: 1.02x slower                                                    |
| regex_compile              | 141 ms                                                 | 145 ms: 1.03x slower                                                     |
| chameleon                  | 6.70 ms                                                | 6.90 ms: 1.03x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                     |
| meteor_contest             | 109 ms                                                 | 113 ms: 1.03x slower                                                     |
| bench_thread_pool          | 834 us                                                 | 864 us: 1.04x slower                                                     |
| genshi_xml                 | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                    |
| pycparser                  | 1.19 sec                                               | 1.23 sec: 1.04x slower                                                   |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                     |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                     |
| hexiom                     | 6.89 ms                                                | 7.17 ms: 1.04x slower                                                    |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.04x slower                                                     |
| sympy_expand               | 484 ms                                                 | 504 ms: 1.04x slower                                                     |
| sqlglot_optimize           | 55.3 ms                                                | 58.1 ms: 1.05x slower                                                    |
| pathlib                    | 18.5 ms                                                | 19.5 ms: 1.05x slower                                                    |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.70 ms: 1.05x slower                                                    |
| xml_etree_process          | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                    |
| html5lib                   | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                    |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                    |
| nqueens                    | 87.9 ms                                                | 93.1 ms: 1.06x slower                                                    |
| 2to3                       | 264 ms                                                 | 281 ms: 1.06x slower                                                     |
| pickle_list                | 4.59 us                                                | 4.90 us: 1.07x slower                                                    |
| xml_etree_generate         | 81.1 ms                                                | 87.8 ms: 1.08x slower                                                    |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 70.4 ms: 1.09x slower                                                    |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                                     |
| genshi_text                | 22.5 ms                                                | 24.7 ms: 1.09x slower                                                    |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.10x slower                                                    |
| pyflate                    | 434 ms                                                 | 478 ms: 1.10x slower                                                     |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                    |
| docutils                   | 2.66 sec                                               | 2.97 sec: 1.11x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 130 ms: 1.12x slower                                                     |
| sqlite_synth               | 2.57 us                                                | 2.90 us: 1.13x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                    |
| scimark_sor                | 121 ms                                                 | 138 ms: 1.14x slower                                                     |
| mypy2                      | 686 ms                                                 | 812 ms: 1.18x slower                                                     |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.22x slower                                                    |
| async_generators           | 374 ms                                                 | 464 ms: 1.24x slower                                                     |
| telco                      | 6.86 ms                                                | 8.58 ms: 1.25x slower                                                    |
| coverage                   | 78.8 ms                                                | 99.0 ms: 1.26x slower                                                    |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 9.57 ms: 1.59x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                             |

Benchmark hidden because not significant (6): fannkuch, pprint_pformat, bench_mp_pool, unpickle_pure_python, json, pprint_safe_repr
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 63.12% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
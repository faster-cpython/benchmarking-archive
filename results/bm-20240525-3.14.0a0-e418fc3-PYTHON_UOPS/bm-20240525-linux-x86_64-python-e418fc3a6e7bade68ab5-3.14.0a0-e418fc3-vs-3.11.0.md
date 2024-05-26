# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-x86_64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.24x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 375 ms: 1.42x slower                                                  |
| chameleon      | 6.70 ms                                                | 8.91 ms: 1.33x slower                                                 |
| docutils       | 2.66 sec                                               | 3.51 sec: 1.32x slower                                                |
| html5lib       | 64.8 ms                                                | 82.2 ms: 1.27x slower                                                 |
| tornado_http   | 98.1 ms                                                | 107 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.28x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 366 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 477 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                |
| async_tree_io              | 1.29 sec                                               | 1.03 sec: 1.25x faster                                                |
| async_tree_none            | 528 ms                                                 | 428 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 620 ms: 1.23x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 531 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 665 ms: 1.13x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                                  |
| float          | 78.9 ms                                                | 130 ms: 1.64x slower                                                  |
| nbody          | 96.0 ms                                                | 193 ms: 2.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.49x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.87 ms: 1.10x slower                                                 |
| regex_dna      | 205 ms                                                 | 235 ms: 1.15x slower                                                  |
| regex_v8       | 22.9 ms                                                | 26.9 ms: 1.18x slower                                                 |
| regex_compile  | 141 ms                                                 | 236 ms: 1.67x slower                                                  |
| Geometric mean | (ref)                                                  | 1.26x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 155 ms: 1.06x faster                                                  |
| unpickle_list        | 5.21 us                                                | 5.17 us: 1.01x faster                                                 |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                                 |
| pickle_dict          | 34.6 us                                                | 35.5 us: 1.03x slower                                                 |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                 |
| pickle               | 11.0 us                                                | 12.2 us: 1.11x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.23 us: 1.14x slower                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 125 ms: 1.16x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 78.3 ms: 1.38x slower                                                 |
| xml_etree_generate   | 81.1 ms                                                | 114 ms: 1.40x slower                                                  |
| tomli_loads          | 2.30 sec                                               | 3.49 sec: 1.51x slower                                                |
| unpickle_pure_python | 242 us                                                 | 396 us: 1.64x slower                                                  |
| pickle_pure_python   | 320 us                                                 | 560 us: 1.75x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.18 ms: 1.19x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 33.5 ms                                                | 49.6 ms: 1.48x slower                                                 |
| genshi_xml      | 53.4 ms                                                | 85.5 ms: 1.60x slower                                                 |
| genshi_text     | 22.5 ms                                                | 41.3 ms: 1.83x slower                                                 |
| mako            | 10.7 ms                                                | 19.9 ms: 1.87x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.69x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 216 us: 2.41x faster                                                  |
| generators                 | 74.9 ms                                                | 31.9 ms: 2.34x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 525 ms: 1.67x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 366 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 477 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                |
| async_tree_io              | 1.29 sec                                               | 1.03 sec: 1.25x faster                                                |
| async_tree_none            | 528 ms                                                 | 428 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 620 ms: 1.23x faster                                                  |
| pylint                     | 476 ms                                                 | 388 ms: 1.23x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 531 ms: 1.20x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 665 ms: 1.13x faster                                                  |
| coroutines                 | 27.0 ms                                                | 24.2 ms: 1.12x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 155 ms: 1.06x faster                                                  |
| pathlib                    | 18.5 ms                                                | 18.0 ms: 1.03x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.89 ms: 1.03x faster                                                 |
| unpickle_list              | 5.21 us                                                | 5.17 us: 1.01x faster                                                 |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                                 |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                                  |
| pickle_dict                | 34.6 us                                                | 35.5 us: 1.03x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                  |
| thrift                     | 784 us                                                 | 831 us: 1.06x slower                                                  |
| logging_simple             | 6.22 us                                                | 6.65 us: 1.07x slower                                                 |
| json                       | 5.24 ms                                                | 5.62 ms: 1.07x slower                                                 |
| dask                       | 365 ms                                                 | 394 ms: 1.08x slower                                                  |
| logging_format             | 6.81 us                                                | 7.42 us: 1.09x slower                                                 |
| tornado_http               | 98.1 ms                                                | 107 ms: 1.09x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                 |
| mdp                        | 2.77 sec                                               | 3.05 sec: 1.10x slower                                                |
| regex_effbot               | 3.51 ms                                                | 3.87 ms: 1.10x slower                                                 |
| pickle                     | 11.0 us                                                | 12.2 us: 1.11x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.23 us: 1.14x slower                                                 |
| regex_dna                  | 205 ms                                                 | 235 ms: 1.15x slower                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 125 ms: 1.16x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 26.9 ms: 1.18x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 199 ms: 1.18x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 996 us: 1.19x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.18 ms: 1.19x slower                                                 |
| coverage                   | 78.8 ms                                                | 94.1 ms: 1.19x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 77.3 ms: 1.20x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 3.13 us: 1.22x slower                                                 |
| raytrace                   | 309 ms                                                 | 384 ms: 1.24x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                 |
| html5lib                   | 64.8 ms                                                | 82.2 ms: 1.27x slower                                                 |
| sympy_expand               | 484 ms                                                 | 615 ms: 1.27x slower                                                  |
| sympy_str                  | 297 ms                                                 | 378 ms: 1.27x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.84 ms: 1.28x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 9.56 ms: 1.31x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 28.2 ms: 1.32x slower                                                 |
| docutils                   | 2.66 sec                                               | 3.51 sec: 1.32x slower                                                |
| async_generators           | 374 ms                                                 | 496 ms: 1.33x slower                                                  |
| chameleon                  | 6.70 ms                                                | 8.91 ms: 1.33x slower                                                 |
| meteor_contest             | 109 ms                                                 | 145 ms: 1.33x slower                                                  |
| sqlglot_normalize          | 113 ms                                                 | 150 ms: 1.33x slower                                                  |
| pycparser                  | 1.19 sec                                               | 1.61 sec: 1.36x slower                                                |
| deltablue                  | 3.92 ms                                                | 5.33 ms: 1.36x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 4.38 us: 1.36x slower                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 75.6 ms: 1.37x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 78.3 ms: 1.38x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 114 ms: 1.40x slower                                                  |
| 2to3                       | 264 ms                                                 | 375 ms: 1.42x slower                                                  |
| richards_super             | 61.9 ms                                                | 88.1 ms: 1.42x slower                                                 |
| sqlglot_transpile          | 1.75 ms                                                | 2.57 ms: 1.47x slower                                                 |
| scimark_sor                | 121 ms                                                 | 179 ms: 1.47x slower                                                  |
| django_template            | 33.5 ms                                                | 49.6 ms: 1.48x slower                                                 |
| sqlglot_parse              | 1.43 ms                                                | 2.14 ms: 1.49x slower                                                 |
| go                         | 149 ms                                                 | 222 ms: 1.50x slower                                                  |
| tomli_loads                | 2.30 sec                                               | 3.49 sec: 1.51x slower                                                |
| deepcopy                   | 365 us                                                 | 554 us: 1.52x slower                                                  |
| chaos                      | 71.9 ms                                                | 109 ms: 1.52x slower                                                  |
| telco                      | 6.86 ms                                                | 10.6 ms: 1.55x slower                                                 |
| comprehensions             | 23.6 us                                                | 37.6 us: 1.59x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 85.5 ms: 1.60x slower                                                 |
| richards                   | 49.8 ms                                                | 81.0 ms: 1.63x slower                                                 |
| unpickle_pure_python       | 242 us                                                 | 396 us: 1.64x slower                                                  |
| float                      | 78.9 ms                                                | 130 ms: 1.64x slower                                                  |
| nqueens                    | 87.9 ms                                                | 145 ms: 1.66x slower                                                  |
| crypto_pyaes               | 76.7 ms                                                | 128 ms: 1.67x slower                                                  |
| regex_compile              | 141 ms                                                 | 236 ms: 1.67x slower                                                  |
| scimark_lu                 | 116 ms                                                 | 196 ms: 1.69x slower                                                  |
| pprint_safe_repr           | 747 ms                                                 | 1.27 sec: 1.69x slower                                                |
| pprint_pformat             | 1.55 sec                                               | 2.63 sec: 1.69x slower                                                |
| fannkuch                   | 405 ms                                                 | 701 ms: 1.73x slower                                                  |
| scimark_fft                | 345 ms                                                 | 598 ms: 1.73x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 8.72 ms: 1.73x slower                                                 |
| pickle_pure_python         | 320 us                                                 | 560 us: 1.75x slower                                                  |
| genshi_text                | 22.5 ms                                                | 41.3 ms: 1.83x slower                                                 |
| mako                       | 10.7 ms                                                | 19.9 ms: 1.87x slower                                                 |
| pyflate                    | 434 ms                                                 | 826 ms: 1.90x slower                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 135 ms: 1.91x slower                                                  |
| deepcopy_memo              | 40.2 us                                                | 77.8 us: 1.94x slower                                                 |
| spectral_norm              | 108 ms                                                 | 216 ms: 2.00x slower                                                  |
| logging_silent             | 111 ns                                                 | 222 ns: 2.00x slower                                                  |
| nbody                      | 96.0 ms                                                | 193 ms: 2.01x slower                                                  |
| hexiom                     | 6.89 ms                                                | 15.0 ms: 2.17x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.24x slower                                                          |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.05x
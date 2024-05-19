# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-x86_64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.28x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 379 ms: 1.43x slower                                                  |
| chameleon      | 6.70 ms                                                | 8.87 ms: 1.32x slower                                                 |
| docutils       | 2.66 sec                                               | 3.57 sec: 1.34x slower                                                |
| html5lib       | 64.8 ms                                                | 85.0 ms: 1.31x slower                                                 |
| tornado_http   | 98.1 ms                                                | 107 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.30x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 409 ms: 1.29x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 998 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 382 ms: 1.29x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 496 ms: 1.26x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 1.05 sec: 1.24x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 624 ms: 1.22x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 532 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 665 ms: 1.13x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 193 ms: 1.00x faster                                                  |
| float          | 78.9 ms                                                | 131 ms: 1.66x slower                                                  |
| nbody          | 96.0 ms                                                | 198 ms: 2.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.51x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.76 ms: 1.07x slower                                                 |
| regex_dna      | 205 ms                                                 | 220 ms: 1.07x slower                                                  |
| regex_v8       | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                 |
| regex_compile  | 141 ms                                                 | 239 ms: 1.69x slower                                                  |
| Geometric mean | (ref)                                                  | 1.21x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 156 ms: 1.05x faster                                                  |
| pickle_dict          | 34.6 us                                                | 33.5 us: 1.03x faster                                                 |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                 |
| unpickle_list        | 5.21 us                                                | 5.70 us: 1.09x slower                                                 |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 128 ms: 1.19x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.54 us: 1.21x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 80.1 ms: 1.41x slower                                                 |
| xml_etree_generate   | 81.1 ms                                                | 116 ms: 1.43x slower                                                  |
| tomli_loads          | 2.30 sec                                               | 3.61 sec: 1.57x slower                                                |
| unpickle_pure_python | 242 us                                                 | 405 us: 1.67x slower                                                  |
| pickle_pure_python   | 320 us                                                 | 556 us: 1.74x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.17 ms: 1.19x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 33.5 ms                                                | 49.6 ms: 1.48x slower                                                 |
| genshi_xml      | 53.4 ms                                                | 86.0 ms: 1.61x slower                                                 |
| genshi_text     | 22.5 ms                                                | 40.6 ms: 1.80x slower                                                 |
| mako            | 10.7 ms                                                | 20.9 ms: 1.96x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.70x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 213 us: 2.43x faster                                                  |
| generators                 | 74.9 ms                                                | 32.1 ms: 2.33x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 532 ms: 1.65x faster                                                  |
| async_tree_none            | 528 ms                                                 | 409 ms: 1.29x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 998 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 382 ms: 1.29x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 496 ms: 1.26x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 1.05 sec: 1.24x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 624 ms: 1.22x faster                                                  |
| pylint                     | 476 ms                                                 | 391 ms: 1.22x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 532 ms: 1.20x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 665 ms: 1.13x faster                                                  |
| coroutines                 | 27.0 ms                                                | 24.8 ms: 1.09x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 156 ms: 1.05x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.85 ms: 1.04x faster                                                 |
| pickle_dict                | 34.6 us                                                | 33.5 us: 1.03x faster                                                 |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.03x faster                                                 |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| pidigits                   | 194 ms                                                 | 193 ms: 1.00x faster                                                  |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.76 ms: 1.07x slower                                                 |
| thrift                     | 784 us                                                 | 841 us: 1.07x slower                                                  |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                 |
| regex_dna                  | 205 ms                                                 | 220 ms: 1.07x slower                                                  |
| logging_simple             | 6.22 us                                                | 6.78 us: 1.09x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.70 us: 1.09x slower                                                 |
| dask                       | 365 ms                                                 | 400 ms: 1.10x slower                                                  |
| tornado_http               | 98.1 ms                                                | 107 ms: 1.10x slower                                                  |
| json                       | 5.24 ms                                                | 5.76 ms: 1.10x slower                                                 |
| logging_format             | 6.81 us                                                | 7.54 us: 1.11x slower                                                 |
| mdp                        | 2.77 sec                                               | 3.08 sec: 1.11x slower                                                |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                 |
| coverage                   | 78.8 ms                                                | 93.1 ms: 1.18x slower                                                 |
| xml_etree_iterparse        | 108 ms                                                 | 128 ms: 1.19x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.17 ms: 1.19x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 203 ms: 1.20x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 1.01 ms: 1.20x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 77.9 ms: 1.21x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.54 us: 1.21x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 3.13 us: 1.22x slower                                                 |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                 |
| raytrace                   | 309 ms                                                 | 379 ms: 1.23x slower                                                  |
| sympy_expand               | 484 ms                                                 | 614 ms: 1.27x slower                                                  |
| sympy_str                  | 297 ms                                                 | 379 ms: 1.27x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.84 ms: 1.28x slower                                                 |
| html5lib                   | 64.8 ms                                                | 85.0 ms: 1.31x slower                                                 |
| chameleon                  | 6.70 ms                                                | 8.87 ms: 1.32x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 28.5 ms: 1.33x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 9.68 ms: 1.33x slower                                                 |
| async_generators           | 374 ms                                                 | 499 ms: 1.33x slower                                                  |
| docutils                   | 2.66 sec                                               | 3.57 sec: 1.34x slower                                                |
| meteor_contest             | 109 ms                                                 | 148 ms: 1.36x slower                                                  |
| deltablue                  | 3.92 ms                                                | 5.36 ms: 1.37x slower                                                 |
| pycparser                  | 1.19 sec                                               | 1.62 sec: 1.37x slower                                                |
| deepcopy_reduce            | 3.22 us                                                | 4.41 us: 1.37x slower                                                 |
| sqlglot_normalize          | 113 ms                                                 | 156 ms: 1.39x slower                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 77.5 ms: 1.40x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 80.1 ms: 1.41x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 116 ms: 1.43x slower                                                  |
| 2to3                       | 264 ms                                                 | 379 ms: 1.43x slower                                                  |
| richards_super             | 61.9 ms                                                | 88.7 ms: 1.43x slower                                                 |
| scimark_sor                | 121 ms                                                 | 179 ms: 1.48x slower                                                  |
| django_template            | 33.5 ms                                                | 49.6 ms: 1.48x slower                                                 |
| go                         | 149 ms                                                 | 222 ms: 1.49x slower                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 2.61 ms: 1.49x slower                                                 |
| sqlglot_parse              | 1.43 ms                                                | 2.15 ms: 1.50x slower                                                 |
| deepcopy                   | 365 us                                                 | 561 us: 1.54x slower                                                  |
| chaos                      | 71.9 ms                                                | 111 ms: 1.55x slower                                                  |
| tomli_loads                | 2.30 sec                                               | 3.61 sec: 1.57x slower                                                |
| genshi_xml                 | 53.4 ms                                                | 86.0 ms: 1.61x slower                                                 |
| comprehensions             | 23.6 us                                                | 38.1 us: 1.61x slower                                                 |
| richards                   | 49.8 ms                                                | 81.7 ms: 1.64x slower                                                 |
| nqueens                    | 87.9 ms                                                | 144 ms: 1.64x slower                                                  |
| float                      | 78.9 ms                                                | 131 ms: 1.66x slower                                                  |
| unpickle_pure_python       | 242 us                                                 | 405 us: 1.67x slower                                                  |
| crypto_pyaes               | 76.7 ms                                                | 128 ms: 1.68x slower                                                  |
| regex_compile              | 141 ms                                                 | 239 ms: 1.69x slower                                                  |
| scimark_lu                 | 116 ms                                                 | 200 ms: 1.72x slower                                                  |
| pprint_pformat             | 1.55 sec                                               | 2.69 sec: 1.73x slower                                                |
| scimark_fft                | 345 ms                                                 | 599 ms: 1.73x slower                                                  |
| pprint_safe_repr           | 747 ms                                                 | 1.30 sec: 1.74x slower                                                |
| pickle_pure_python         | 320 us                                                 | 556 us: 1.74x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 8.96 ms: 1.78x slower                                                 |
| fannkuch                   | 405 ms                                                 | 726 ms: 1.79x slower                                                  |
| genshi_text                | 22.5 ms                                                | 40.6 ms: 1.80x slower                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 136 ms: 1.93x slower                                                  |
| deepcopy_memo              | 40.2 us                                                | 77.9 us: 1.94x slower                                                 |
| pyflate                    | 434 ms                                                 | 849 ms: 1.96x slower                                                  |
| mako                       | 10.7 ms                                                | 20.9 ms: 1.96x slower                                                 |
| logging_silent             | 111 ns                                                 | 223 ns: 2.01x slower                                                  |
| spectral_norm              | 108 ms                                                 | 223 ms: 2.06x slower                                                  |
| nbody                      | 96.0 ms                                                | 198 ms: 2.06x slower                                                  |
| hexiom                     | 6.89 ms                                                | 15.2 ms: 2.21x slower                                                 |
| telco                      | 6.86 ms                                                | 182 ms: 26.55x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.28x slower                                                          |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.05x
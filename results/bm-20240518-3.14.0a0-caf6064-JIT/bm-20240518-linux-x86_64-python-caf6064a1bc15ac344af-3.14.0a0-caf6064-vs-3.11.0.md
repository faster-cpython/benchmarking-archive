# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-x86_64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.03x faster
- HPT reliability: 98.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| chameleon      | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                 |
| docutils       | 2.66 sec                                               | 2.94 sec: 1.11x slower                                                |
| html5lib       | 64.8 ms                                                | 66.0 ms: 1.02x slower                                                 |
| tornado_http   | 98.1 ms                                                | 96.6 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 455 ms: 1.38x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 945 ms: 1.36x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.33x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 986 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 596 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 625 ms: 1.20x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.4 ms: 1.19x faster                                                 |
| float          | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                 |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.02x faster                                                  |
| regex_effbot   | 3.51 ms                                                | 3.47 ms: 1.01x faster                                                 |
| regex_dna      | 205 ms                                                 | 209 ms: 1.02x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.0 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                 |
| tomli_loads          | 2.30 sec                                               | 1.94 sec: 1.19x faster                                                |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                                  |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                 |
| pickle_dict          | 34.6 us                                                | 34.2 us: 1.01x faster                                                 |
| xml_etree_generate   | 81.1 ms                                                | 82.4 ms: 1.02x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 58.1 ms: 1.02x slower                                                 |
| unpickle_list        | 5.21 us                                                | 5.38 us: 1.03x slower                                                 |
| pickle               | 11.0 us                                                | 11.6 us: 1.05x slower                                                 |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.57 us: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.62 ms: 1.11x faster                                                 |
| genshi_xml      | 53.4 ms                                                | 58.0 ms: 1.08x slower                                                 |
| django_template | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                 |
| genshi_text     | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 173 us: 3.00x faster                                                  |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 522 ms: 1.68x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                |
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 455 ms: 1.38x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 945 ms: 1.36x faster                                                  |
| pylint                     | 476 ms                                                 | 352 ms: 1.35x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.33x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 986 ms: 1.31x faster                                                  |
| richards_super             | 61.9 ms                                                | 48.0 ms: 1.29x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 596 ms: 1.28x faster                                                  |
| chaos                      | 71.9 ms                                                | 59.5 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 625 ms: 1.20x faster                                                  |
| nbody                      | 96.0 ms                                                | 80.4 ms: 1.19x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 1.94 sec: 1.19x faster                                                |
| richards                   | 49.8 ms                                                | 42.1 ms: 1.18x faster                                                 |
| coroutines                 | 27.0 ms                                                | 23.2 ms: 1.17x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 66.7 ms: 1.15x faster                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.45 ms: 1.13x faster                                                 |
| fannkuch                   | 405 ms                                                 | 359 ms: 1.13x faster                                                  |
| pathlib                    | 18.5 ms                                                | 16.5 ms: 1.12x faster                                                 |
| raytrace                   | 309 ms                                                 | 275 ms: 1.12x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 63.1 ms: 1.12x faster                                                 |
| mako                       | 10.7 ms                                                | 9.62 ms: 1.11x faster                                                 |
| scimark_fft                | 345 ms                                                 | 313 ms: 1.10x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                 |
| float                      | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                 |
| logging_simple             | 6.22 us                                                | 5.69 us: 1.09x faster                                                 |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| logging_format             | 6.81 us                                                | 6.31 us: 1.08x faster                                                 |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.08x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                                |
| spectral_norm              | 108 ms                                                 | 101 ms: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 37.7 us: 1.06x faster                                                 |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.47 sec: 1.06x faster                                                |
| deltablue                  | 3.92 ms                                                | 3.71 ms: 1.06x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.84 ms: 1.04x faster                                                 |
| pprint_safe_repr           | 747 ms                                                 | 721 ms: 1.04x faster                                                  |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.68 ms: 1.03x faster                                                 |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                |
| regex_compile              | 141 ms                                                 | 138 ms: 1.02x faster                                                  |
| tornado_http               | 98.1 ms                                                | 96.6 ms: 1.02x faster                                                 |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                  |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                 |
| regex_effbot               | 3.51 ms                                                | 3.47 ms: 1.01x faster                                                 |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                                 |
| nqueens                    | 87.9 ms                                                | 87.3 ms: 1.01x faster                                                 |
| pyflate                    | 434 ms                                                 | 437 ms: 1.01x slower                                                  |
| sympy_str                  | 297 ms                                                 | 300 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                  |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                  |
| json                       | 5.24 ms                                                | 5.32 ms: 1.01x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 82.4 ms: 1.02x slower                                                 |
| html5lib                   | 64.8 ms                                                | 66.0 ms: 1.02x slower                                                 |
| regex_dna                  | 205 ms                                                 | 209 ms: 1.02x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 58.1 ms: 1.02x slower                                                 |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.02x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 860 us: 1.03x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.38 us: 1.03x slower                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                                 |
| dask                       | 365 ms                                                 | 378 ms: 1.04x slower                                                  |
| sympy_expand               | 484 ms                                                 | 508 ms: 1.05x slower                                                  |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 24.0 ms: 1.05x slower                                                 |
| pickle                     | 11.0 us                                                | 11.6 us: 1.05x slower                                                 |
| chameleon                  | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                 |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 69.5 ms: 1.08x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 58.0 ms: 1.08x slower                                                 |
| django_template            | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                 |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.10x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                 |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                 |
| docutils                   | 2.66 sec                                               | 2.94 sec: 1.11x slower                                                |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.57 us: 1.21x slower                                                 |
| coverage                   | 78.8 ms                                                | 95.9 ms: 1.22x slower                                                 |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                  |
| flaskblogging              | 7.28 ms                                                | 9.18 ms: 1.26x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                                 |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                 |
| telco                      | 6.86 ms                                                | 172 ms: 25.05x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): bench_mp_pool, deepcopy
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.91% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-x86_64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.03x faster
- HPT reliability: 99.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.02x slower                                                  |
| chameleon      | 6.70 ms                                                | 6.97 ms: 1.04x slower                                                 |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                |
| html5lib       | 64.8 ms                                                | 65.6 ms: 1.01x slower                                                 |
| tornado_http   | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 362 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 471 ms: 1.36x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 969 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.22x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.2 ms: 1.10x faster                                                 |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                  |
| float          | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                  |
| regex_effbot   | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                 |
| regex_dna      | 205 ms                                                 | 219 ms: 1.07x slower                                                  |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                 |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.11 sec: 1.09x faster                                                |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                  |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| pickle_dict          | 34.6 us                                                | 34.2 us: 1.01x faster                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                  |
| unpickle_list        | 5.21 us                                                | 5.47 us: 1.05x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 60.1 ms: 1.06x slower                                                 |
| xml_etree_generate   | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                 |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.61 us: 1.22x slower                                                 |
| unpickle             | 13.8 us                                                | 16.9 us: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.10 ms: 1.18x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.21x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.0 ms: 1.05x faster                                                 |
| django_template | 33.5 ms                                                | 34.3 ms: 1.02x slower                                                 |
| genshi_text     | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                 |
| mako            | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-linux-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 167 us: 3.11x faster                                                  |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                  |
| async_tree_none            | 528 ms                                                 | 362 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.41x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 471 ms: 1.36x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 969 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.22x faster                                                  |
| chaos                      | 71.9 ms                                                | 59.8 ms: 1.20x faster                                                 |
| deltablue                  | 3.92 ms                                                | 3.29 ms: 1.19x faster                                                 |
| coroutines                 | 27.0 ms                                                | 23.2 ms: 1.17x faster                                                 |
| raytrace                   | 309 ms                                                 | 266 ms: 1.16x faster                                                  |
| richards_super             | 61.9 ms                                                | 54.5 ms: 1.13x faster                                                 |
| pathlib                    | 18.5 ms                                                | 16.3 ms: 1.13x faster                                                 |
| nqueens                    | 87.9 ms                                                | 79.6 ms: 1.10x faster                                                 |
| nbody                      | 96.0 ms                                                | 87.2 ms: 1.10x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                 |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.30 ms: 1.09x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 2.11 sec: 1.09x faster                                                |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.72 us: 1.09x faster                                                 |
| sqlglot_transpile          | 1.75 ms                                                | 1.61 ms: 1.08x faster                                                 |
| logging_format             | 6.81 us                                                | 6.29 us: 1.08x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                                |
| sympy_str                  | 297 ms                                                 | 278 ms: 1.07x faster                                                  |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                 |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                  |
| genshi_xml                 | 53.4 ms                                                | 51.0 ms: 1.05x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 73.4 ms: 1.04x faster                                                 |
| tornado_http               | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                 |
| sympy_expand               | 484 ms                                                 | 467 ms: 1.04x faster                                                  |
| richards                   | 49.8 ms                                                | 48.0 ms: 1.04x faster                                                 |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.04x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 68.4 ms: 1.03x faster                                                 |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 39.1 us: 1.03x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.90 ms: 1.03x faster                                                 |
| go                         | 149 ms                                                 | 145 ms: 1.02x faster                                                  |
| float                      | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 54.7 ms: 1.01x faster                                                 |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                |
| deepcopy                   | 365 us                                                 | 361 us: 1.01x faster                                                  |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                                 |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                  |
| fannkuch                   | 405 ms                                                 | 402 ms: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                 |
| bench_thread_pool          | 834 us                                                 | 832 us: 1.00x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 751 ms: 1.01x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                 |
| html5lib                   | 64.8 ms                                                | 65.6 ms: 1.01x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.26 us: 1.01x slower                                                 |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.01x slower                                                  |
| 2to3                       | 264 ms                                                 | 268 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.11 ms: 1.02x slower                                                 |
| django_template            | 33.5 ms                                                | 34.3 ms: 1.02x slower                                                 |
| genshi_text                | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 66.4 ms: 1.03x slower                                                 |
| thrift                     | 784 us                                                 | 806 us: 1.03x slower                                                  |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                  |
| spectral_norm              | 108 ms                                                 | 111 ms: 1.03x slower                                                  |
| chameleon                  | 6.70 ms                                                | 6.97 ms: 1.04x slower                                                 |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                |
| scimark_sor                | 121 ms                                                 | 127 ms: 1.05x slower                                                  |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.47 us: 1.05x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 60.1 ms: 1.06x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                 |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                 |
| regex_dna                  | 205 ms                                                 | 219 ms: 1.07x slower                                                  |
| scimark_fft                | 345 ms                                                 | 377 ms: 1.09x slower                                                  |
| pyflate                    | 434 ms                                                 | 480 ms: 1.11x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                                 |
| coverage                   | 78.8 ms                                                | 92.8 ms: 1.18x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.10 ms: 1.18x slower                                                 |
| async_generators           | 374 ms                                                 | 447 ms: 1.20x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.21x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 8.89 ms: 1.22x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.61 us: 1.22x slower                                                 |
| unpickle                   | 13.8 us                                                | 16.9 us: 1.22x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                                 |
| telco                      | 6.86 ms                                                | 173 ms: 25.30x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (3): scimark_lu, pycparser, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.37% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
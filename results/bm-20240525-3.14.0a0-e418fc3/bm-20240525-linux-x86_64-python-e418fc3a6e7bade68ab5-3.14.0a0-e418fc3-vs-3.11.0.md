# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-x86_64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.07x faster
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                  |
| chameleon      | 6.70 ms                                                | 7.01 ms: 1.05x slower                                                 |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.05x slower                                                |
| html5lib       | 64.8 ms                                                | 67.1 ms: 1.03x slower                                                 |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 352 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 452 ms: 1.39x faster                                                  |
| async_tree_none            | 528 ms                                                 | 381 ms: 1.38x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 967 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 588 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 84.6 ms: 1.13x faster                                                 |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                  |
| float          | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                  |
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                 |
| regex_dna      | 205 ms                                                 | 222 ms: 1.08x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                 |
| unpickle_pure_python | 242 us                                                 | 214 us: 1.13x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                  |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| unpickle_list        | 5.21 us                                                | 5.35 us: 1.03x slower                                                 |
| pickle_dict          | 34.6 us                                                | 35.7 us: 1.03x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 59.9 ms: 1.05x slower                                                 |
| xml_etree_generate   | 81.1 ms                                                | 86.2 ms: 1.06x slower                                                 |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                 |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.20 us: 1.13x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.3 ms: 1.04x faster                                                 |
| mako            | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                 |
| django_template | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                 |
| genshi_text     | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 166 us: 3.12x faster                                                  |
| generators                 | 74.9 ms                                                | 28.6 ms: 2.62x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 352 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 452 ms: 1.39x faster                                                  |
| async_tree_none            | 528 ms                                                 | 381 ms: 1.38x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 967 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 588 ms: 1.29x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.26 ms: 1.20x faster                                                 |
| chaos                      | 71.9 ms                                                | 60.4 ms: 1.19x faster                                                 |
| raytrace                   | 309 ms                                                 | 262 ms: 1.18x faster                                                  |
| coroutines                 | 27.0 ms                                                | 23.4 ms: 1.15x faster                                                 |
| pathlib                    | 18.5 ms                                                | 16.2 ms: 1.14x faster                                                 |
| nbody                      | 96.0 ms                                                | 84.6 ms: 1.13x faster                                                 |
| richards_super             | 61.9 ms                                                | 54.8 ms: 1.13x faster                                                 |
| unpickle_pure_python       | 242 us                                                 | 214 us: 1.13x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.12 ms: 1.13x faster                                                 |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                 |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.08x faster                                                 |
| nqueens                    | 87.9 ms                                                | 81.8 ms: 1.07x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                |
| logging_simple             | 6.22 us                                                | 5.80 us: 1.07x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                  |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                  |
| logging_format             | 6.81 us                                                | 6.43 us: 1.06x faster                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 67.0 ms: 1.06x faster                                                 |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.81 ms: 1.05x faster                                                 |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                  |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                 |
| genshi_xml                 | 53.4 ms                                                | 51.3 ms: 1.04x faster                                                 |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 74.4 ms: 1.03x faster                                                 |
| deepcopy_memo              | 40.2 us                                                | 39.0 us: 1.03x faster                                                 |
| fannkuch                   | 405 ms                                                 | 394 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.03x faster                                                |
| scimark_lu                 | 116 ms                                                 | 113 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                                  |
| richards                   | 49.8 ms                                                | 48.6 ms: 1.02x faster                                                 |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                  |
| float                      | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                 |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                |
| sympy_expand               | 484 ms                                                 | 474 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                  |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| pprint_safe_repr           | 747 ms                                                 | 741 ms: 1.01x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.76 sec: 1.01x faster                                                |
| sqlglot_optimize           | 55.3 ms                                                | 55.0 ms: 1.01x faster                                                 |
| bench_thread_pool          | 834 us                                                 | 830 us: 1.01x faster                                                  |
| deepcopy                   | 365 us                                                 | 364 us: 1.00x faster                                                  |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.09 ms: 1.01x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 65.7 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.28 us: 1.02x slower                                                 |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.35 us: 1.03x slower                                                 |
| thrift                     | 784 us                                                 | 805 us: 1.03x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                  |
| pickle_dict                | 34.6 us                                                | 35.7 us: 1.03x slower                                                 |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                 |
| html5lib                   | 64.8 ms                                                | 67.1 ms: 1.03x slower                                                 |
| scimark_fft                | 345 ms                                                 | 359 ms: 1.04x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.05x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.01 ms: 1.05x slower                                                 |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.05x slower                                                  |
| django_template            | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                 |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 59.9 ms: 1.05x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 86.2 ms: 1.06x slower                                                 |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                 |
| regex_dna                  | 205 ms                                                 | 222 ms: 1.08x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                 |
| pyflate                    | 434 ms                                                 | 472 ms: 1.09x slower                                                  |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.10x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.20 us: 1.13x slower                                                 |
| coverage                   | 78.8 ms                                                | 91.1 ms: 1.16x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.98 us: 1.16x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                 |
| async_generators           | 374 ms                                                 | 452 ms: 1.21x slower                                                  |
| flaskblogging              | 7.28 ms                                                | 8.92 ms: 1.23x slower                                                 |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                 |
| telco                      | 6.86 ms                                                | 8.59 ms: 1.25x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (3): bench_mp_pool, json, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.85% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
# Results vs. 3.11.0

- fork: python
- ref: ec9d12be9648ee60a2eb
- machine: linux-x86_64
- commit hash: ec9d12b
- commit date: 2024-05-10
- overall geometric mean: 1.03x faster
- HPT reliability: 96.87%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                                  |
| chameleon      | 6.70 ms                                                | 7.08 ms: 1.06x slower                                                 |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                |
| html5lib       | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                 |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.36x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 955 ms: 1.35x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.33x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 981 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.22x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.0 ms: 1.09x faster                                                 |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                  |
| float          | 78.9 ms                                                | 78.6 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.04x faster                                                  |
| regex_dna      | 205 ms                                                 | 215 ms: 1.05x slower                                                  |
| regex_effbot   | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                 |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                 |
| tomli_loads          | 2.30 sec                                               | 2.10 sec: 1.10x faster                                                |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 310 us: 1.03x faster                                                  |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                                 |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.02x slower                                                 |
| unpickle_list        | 5.21 us                                                | 5.34 us: 1.02x slower                                                 |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 61.5 ms: 1.08x slower                                                 |
| xml_etree_generate   | 81.1 ms                                                | 89.0 ms: 1.10x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.29 us: 1.15x slower                                                 |
| unpickle             | 13.8 us                                                | 16.1 us: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.3 ms: 1.21x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.7 ms: 1.03x faster                                                 |
| mako            | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                 |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                 |
| genshi_text     | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 167 us: 3.11x faster                                                  |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.56x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                  |
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.36x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 955 ms: 1.35x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.33x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 981 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.22x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.27 ms: 1.20x faster                                                 |
| chaos                      | 71.9 ms                                                | 60.3 ms: 1.19x faster                                                 |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.18x faster                                                 |
| raytrace                   | 309 ms                                                 | 267 ms: 1.16x faster                                                  |
| richards_super             | 61.9 ms                                                | 54.5 ms: 1.14x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 2.10 sec: 1.10x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.28 ms: 1.10x faster                                                 |
| nqueens                    | 87.9 ms                                                | 80.3 ms: 1.09x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.67 ms: 1.09x faster                                                 |
| nbody                      | 96.0 ms                                                | 88.0 ms: 1.09x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.57 sec: 1.08x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                 |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                                 |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                  |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                  |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                  |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                                 |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                 |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                 |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                 |
| regex_compile              | 141 ms                                                 | 135 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 67.9 ms: 1.04x faster                                                 |
| richards                   | 49.8 ms                                                | 48.0 ms: 1.04x faster                                                 |
| genshi_xml                 | 53.4 ms                                                | 51.7 ms: 1.03x faster                                                 |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 310 us: 1.03x faster                                                  |
| sympy_expand               | 484 ms                                                 | 469 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 74.5 ms: 1.03x faster                                                 |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                |
| fannkuch                   | 405 ms                                                 | 400 ms: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                 |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                                 |
| float                      | 78.9 ms                                                | 78.6 ms: 1.00x faster                                                 |
| pprint_pformat             | 1.55 sec                                               | 1.56 sec: 1.00x slower                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.10 ms: 1.01x slower                                                 |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.02x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                                 |
| dask                       | 365 ms                                                 | 371 ms: 1.02x slower                                                  |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 65.8 ms: 1.02x slower                                                 |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                                  |
| pprint_safe_repr           | 747 ms                                                 | 764 ms: 1.02x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.34 us: 1.02x slower                                                 |
| json                       | 5.24 ms                                                | 5.44 ms: 1.04x slower                                                 |
| mako                       | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                 |
| thrift                     | 784 us                                                 | 820 us: 1.05x slower                                                  |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                 |
| regex_dna                  | 205 ms                                                 | 215 ms: 1.05x slower                                                  |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                 |
| html5lib                   | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                 |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.08 ms: 1.06x slower                                                 |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.06x slower                                                  |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                 |
| scimark_sor                | 121 ms                                                 | 130 ms: 1.07x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 61.5 ms: 1.08x slower                                                 |
| pyflate                    | 434 ms                                                 | 474 ms: 1.09x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 89.0 ms: 1.10x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                 |
| scimark_fft                | 345 ms                                                 | 382 ms: 1.10x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.29 us: 1.15x slower                                                 |
| unpickle                   | 13.8 us                                                | 16.1 us: 1.16x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                 |
| coverage                   | 78.8 ms                                                | 93.8 ms: 1.19x slower                                                 |
| async_generators           | 374 ms                                                 | 446 ms: 1.19x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.3 ms: 1.21x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 8.94 ms: 1.23x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.25x slower                                                 |
| telco                      | 6.86 ms                                                | 173 ms: 25.27x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (7): xml_etree_parse, xml_etree_iterparse, bench_thread_pool, sqlglot_optimize, deepcopy, deepcopy_memo, scimark_lu
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.87% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
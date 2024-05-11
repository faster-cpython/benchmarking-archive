# Results vs. 3.11.0

- fork: python
- ref: ec9d12be9648ee60a2eb
- machine: linux-x86_64
- commit hash: ec9d12b
- commit date: 2024-05-10
- overall geometric mean: 1.03x faster
- HPT reliability: 97.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| chameleon      | 6.70 ms                                                | 7.00 ms: 1.04x slower                                                 |
| docutils       | 2.66 sec                                               | 2.97 sec: 1.11x slower                                                |
| html5lib       | 64.8 ms                                                | 67.7 ms: 1.05x slower                                                 |
| tornado_http   | 98.1 ms                                                | 97.6 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 365 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 943 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.36x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 986 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 597 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 627 ms: 1.19x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.9 ms: 1.19x faster                                                 |
| float          | 78.9 ms                                                | 71.6 ms: 1.10x faster                                                 |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.01x faster                                                  |
| regex_effbot   | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                 |
| regex_dna      | 205 ms                                                 | 214 ms: 1.05x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.3 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                 |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                  |
| pickle_dict          | 34.6 us                                                | 33.5 us: 1.03x faster                                                 |
| json_loads           | 29.2 us                                                | 29.1 us: 1.00x faster                                                 |
| xml_etree_generate   | 81.1 ms                                                | 83.1 ms: 1.03x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 59.1 ms: 1.04x slower                                                 |
| unpickle_list        | 5.21 us                                                | 5.44 us: 1.04x slower                                                 |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                 |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.47 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                 |
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.56 ms: 1.11x faster                                                 |
| django_template | 33.5 ms                                                | 36.3 ms: 1.08x slower                                                 |
| genshi_xml      | 53.4 ms                                                | 57.9 ms: 1.08x slower                                                 |
| genshi_text     | 22.5 ms                                                | 24.7 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 171 us: 3.04x faster                                                  |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 522 ms: 1.68x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                |
| async_tree_none            | 528 ms                                                 | 365 ms: 1.44x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 943 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.36x faster                                                  |
| pylint                     | 476 ms                                                 | 354 ms: 1.34x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 986 ms: 1.31x faster                                                  |
| richards_super             | 61.9 ms                                                | 47.6 ms: 1.30x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 597 ms: 1.27x faster                                                  |
| chaos                      | 71.9 ms                                                | 59.3 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 627 ms: 1.19x faster                                                  |
| richards                   | 49.8 ms                                                | 41.8 ms: 1.19x faster                                                 |
| nbody                      | 96.0 ms                                                | 80.9 ms: 1.19x faster                                                 |
| coroutines                 | 27.0 ms                                                | 22.9 ms: 1.18x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                |
| crypto_pyaes               | 76.7 ms                                                | 67.9 ms: 1.13x faster                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.49 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 63.4 ms: 1.12x faster                                                 |
| mako                       | 10.7 ms                                                | 9.56 ms: 1.11x faster                                                 |
| raytrace                   | 309 ms                                                 | 278 ms: 1.11x faster                                                  |
| float                      | 78.9 ms                                                | 71.6 ms: 1.10x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                 |
| fannkuch                   | 405 ms                                                 | 371 ms: 1.09x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.73 us: 1.08x faster                                                 |
| logging_format             | 6.81 us                                                | 6.28 us: 1.08x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                  |
| scimark_fft                | 345 ms                                                 | 319 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 37.9 us: 1.06x faster                                                 |
| spectral_norm              | 108 ms                                                 | 102 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 708 ms: 1.06x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.73 ms: 1.05x faster                                                 |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.58 ms: 1.05x faster                                                 |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.04x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.87 ms: 1.04x faster                                                 |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                |
| pickle_dict                | 34.6 us                                                | 33.5 us: 1.03x faster                                                 |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.72 sec: 1.02x faster                                                |
| regex_compile              | 141 ms                                                 | 139 ms: 1.01x faster                                                  |
| nqueens                    | 87.9 ms                                                | 87.0 ms: 1.01x faster                                                 |
| tornado_http               | 98.1 ms                                                | 97.6 ms: 1.01x faster                                                 |
| json_loads                 | 29.2 us                                                | 29.1 us: 1.00x faster                                                 |
| go                         | 149 ms                                                 | 149 ms: 1.00x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                 |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                  |
| sympy_str                  | 297 ms                                                 | 301 ms: 1.01x slower                                                  |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 56.5 ms: 1.02x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 83.1 ms: 1.03x slower                                                 |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                  |
| deepcopy                   | 365 us                                                 | 378 us: 1.04x slower                                                  |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 59.1 ms: 1.04x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.44 us: 1.04x slower                                                 |
| chameleon                  | 6.70 ms                                                | 7.00 ms: 1.04x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.36 us: 1.05x slower                                                 |
| html5lib                   | 64.8 ms                                                | 67.7 ms: 1.05x slower                                                 |
| regex_dna                  | 205 ms                                                 | 214 ms: 1.05x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 877 us: 1.05x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                                 |
| sympy_expand               | 484 ms                                                 | 510 ms: 1.05x slower                                                  |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| thrift                     | 784 us                                                 | 830 us: 1.06x slower                                                  |
| pyflate                    | 434 ms                                                 | 459 ms: 1.06x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 24.3 ms: 1.06x slower                                                 |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                 |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 69.6 ms: 1.08x slower                                                 |
| django_template            | 33.5 ms                                                | 36.3 ms: 1.08x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 57.9 ms: 1.08x slower                                                 |
| genshi_text                | 22.5 ms                                                | 24.7 ms: 1.10x slower                                                 |
| docutils                   | 2.66 sec                                               | 2.97 sec: 1.11x slower                                                |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.12x slower                                                 |
| scimark_sor                | 121 ms                                                 | 136 ms: 1.12x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.47 us: 1.19x slower                                                 |
| coverage                   | 78.8 ms                                                | 95.1 ms: 1.21x slower                                                 |
| async_generators           | 374 ms                                                 | 466 ms: 1.25x slower                                                  |
| flaskblogging              | 7.28 ms                                                | 9.23 ms: 1.27x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.83 ms: 1.28x slower                                                 |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                 |
| telco                      | 6.86 ms                                                | 173 ms: 25.20x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): sqlglot_normalize, bench_mp_pool
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.16% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
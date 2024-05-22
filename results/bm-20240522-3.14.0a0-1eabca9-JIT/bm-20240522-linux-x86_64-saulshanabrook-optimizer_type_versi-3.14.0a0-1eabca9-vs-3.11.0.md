# Results vs. 3.11.0

- fork: saulshanabrook
- ref: optimizer_type_versi
- machine: linux-x86_64
- commit hash: 1eabca9
- commit date: 2024-05-22
- overall geometric mean: 1.07x faster
- HPT reliability: 98.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.05x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.00 ms: 1.04x slower                                                         |
| docutils       | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                        |
| html5lib       | 64.8 ms                                                | 67.0 ms: 1.03x slower                                                         |
| tornado_http   | 98.1 ms                                                | 96.7 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                                          |
| async_tree_none            | 528 ms                                                 | 379 ms: 1.39x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 943 ms: 1.36x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 958 ms: 1.35x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 581 ms: 1.31x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.1 ms: 1.18x faster                                                         |
| float          | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                         |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.03x faster                                                          |
| regex_effbot   | 3.51 ms                                                | 3.58 ms: 1.02x slower                                                         |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                         |
| regex_dna      | 205 ms                                                 | 228 ms: 1.12x slower                                                          |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.2 ms: 1.31x faster                                                         |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.17x faster                                                        |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                          |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.09x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 296 us: 1.08x faster                                                          |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| unpickle_list        | 5.21 us                                                | 5.17 us: 1.01x faster                                                         |
| xml_etree_generate   | 81.1 ms                                                | 83.1 ms: 1.02x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 58.6 ms: 1.03x slower                                                         |
| pickle_dict          | 34.6 us                                                | 36.8 us: 1.06x slower                                                         |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                                         |
| pickle               | 11.0 us                                                | 12.2 us: 1.11x slower                                                         |
| pickle_list          | 4.59 us                                                | 5.36 us: 1.17x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.62 ms: 1.27x slower                                                         |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.99 ms: 1.07x faster                                                         |
| genshi_xml      | 53.4 ms                                                | 56.9 ms: 1.06x slower                                                         |
| genshi_text     | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                         |
| django_template | 33.5 ms                                                | 36.4 ms: 1.08x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-1eabca9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 173 us: 3.01x faster                                                          |
| generators                 | 74.9 ms                                                | 30.5 ms: 2.46x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 521 ms: 1.68x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                        |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                          |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.43x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                                          |
| async_tree_none            | 528 ms                                                 | 379 ms: 1.39x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 943 ms: 1.36x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 958 ms: 1.35x faster                                                          |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 581 ms: 1.31x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.2 ms: 1.31x faster                                                         |
| richards_super             | 61.9 ms                                                | 48.2 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                          |
| chaos                      | 71.9 ms                                                | 59.6 ms: 1.21x faster                                                         |
| richards                   | 49.8 ms                                                | 41.7 ms: 1.19x faster                                                         |
| nbody                      | 96.0 ms                                                | 81.1 ms: 1.18x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.17x faster                                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.33 ms: 1.16x faster                                                         |
| coroutines                 | 27.0 ms                                                | 23.5 ms: 1.15x faster                                                         |
| fannkuch                   | 405 ms                                                 | 354 ms: 1.15x faster                                                          |
| crypto_pyaes               | 76.7 ms                                                | 66.9 ms: 1.15x faster                                                         |
| scimark_monte_carlo        | 70.7 ms                                                | 61.9 ms: 1.14x faster                                                         |
| pathlib                    | 18.5 ms                                                | 16.5 ms: 1.12x faster                                                         |
| raytrace                   | 309 ms                                                 | 277 ms: 1.11x faster                                                          |
| scimark_fft                | 345 ms                                                 | 311 ms: 1.11x faster                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                          |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.09x faster                                                          |
| float                      | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                         |
| pickle_pure_python         | 320 us                                                 | 296 us: 1.08x faster                                                          |
| logging_simple             | 6.22 us                                                | 5.76 us: 1.08x faster                                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.08x faster                                                         |
| pprint_safe_repr           | 747 ms                                                 | 694 ms: 1.08x faster                                                          |
| deepcopy_memo              | 40.2 us                                                | 37.3 us: 1.08x faster                                                         |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| spectral_norm              | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| mako                       | 10.7 ms                                                | 9.99 ms: 1.07x faster                                                         |
| pprint_pformat             | 1.55 sec                                               | 1.46 sec: 1.07x faster                                                        |
| logging_format             | 6.81 us                                                | 6.39 us: 1.07x faster                                                         |
| deltablue                  | 3.92 ms                                                | 3.69 ms: 1.06x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.80 ms: 1.06x faster                                                         |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                          |
| hexiom                     | 6.89 ms                                                | 6.62 ms: 1.04x faster                                                         |
| pycparser                  | 1.19 sec                                               | 1.14 sec: 1.04x faster                                                        |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                          |
| regex_compile              | 141 ms                                                 | 138 ms: 1.03x faster                                                          |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| tornado_http               | 98.1 ms                                                | 96.7 ms: 1.01x faster                                                         |
| nqueens                    | 87.9 ms                                                | 86.9 ms: 1.01x faster                                                         |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                          |
| unpickle_list              | 5.21 us                                                | 5.17 us: 1.01x faster                                                         |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x slower                                                          |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                        |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                          |
| pyflate                    | 434 ms                                                 | 439 ms: 1.01x slower                                                          |
| sympy_str                  | 297 ms                                                 | 301 ms: 1.01x slower                                                          |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                                          |
| regex_effbot               | 3.51 ms                                                | 3.58 ms: 1.02x slower                                                         |
| xml_etree_generate         | 81.1 ms                                                | 83.1 ms: 1.02x slower                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 56.8 ms: 1.03x slower                                                         |
| xml_etree_process          | 56.9 ms                                                | 58.6 ms: 1.03x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.32 us: 1.03x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 862 us: 1.03x slower                                                          |
| html5lib                   | 64.8 ms                                                | 67.0 ms: 1.03x slower                                                         |
| dask                       | 365 ms                                                 | 378 ms: 1.03x slower                                                          |
| chameleon                  | 6.70 ms                                                | 7.00 ms: 1.04x slower                                                         |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                         |
| 2to3                       | 264 ms                                                 | 278 ms: 1.05x slower                                                          |
| sympy_expand               | 484 ms                                                 | 511 ms: 1.05x slower                                                          |
| thrift                     | 784 us                                                 | 833 us: 1.06x slower                                                          |
| genshi_xml                 | 53.4 ms                                                | 56.9 ms: 1.06x slower                                                         |
| pickle_dict                | 34.6 us                                                | 36.8 us: 1.06x slower                                                         |
| scimark_lu                 | 116 ms                                                 | 124 ms: 1.06x slower                                                          |
| dulwich_log                | 64.6 ms                                                | 69.0 ms: 1.07x slower                                                         |
| genshi_text                | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                         |
| django_template            | 33.5 ms                                                | 36.4 ms: 1.08x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                         |
| docutils                   | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                        |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                                         |
| pickle                     | 11.0 us                                                | 12.2 us: 1.11x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.12x slower                                                         |
| regex_dna                  | 205 ms                                                 | 228 ms: 1.12x slower                                                          |
| scimark_sor                | 121 ms                                                 | 138 ms: 1.14x slower                                                          |
| pickle_list                | 4.59 us                                                | 5.36 us: 1.17x slower                                                         |
| coverage                   | 78.8 ms                                                | 92.5 ms: 1.17x slower                                                         |
| telco                      | 6.86 ms                                                | 8.19 ms: 1.19x slower                                                         |
| async_generators           | 374 ms                                                 | 460 ms: 1.23x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                         |
| flaskblogging              | 7.28 ms                                                | 9.18 ms: 1.26x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.62 ms: 1.27x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                  |

Benchmark hidden because not significant (3): json, bench_mp_pool, deepcopy
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.24% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x
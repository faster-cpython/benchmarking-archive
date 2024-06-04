# Results vs. 3.11.0

- fork: python
- ref: 6b10467fbc0b67bf217e
- machine: linux-aarch64
- commit hash: 6b10467
- commit date: 2024-06-03
- overall geometric mean: 1.05x faster
- HPT reliability: 99.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 305 ms: 1.02x slower                                                     |
| chameleon      | 8.29 ms                                                               | 8.89 ms: 1.07x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.08 sec: 1.06x slower                                                   |
| html5lib       | 65.3 ms                                                               | 67.4 ms: 1.03x slower                                                    |
| tornado_http   | 140 ms                                                                | 127 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 491 ms: 1.43x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 648 ms: 1.35x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.21 sec: 1.32x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 481 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 787 ms: 1.21x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.28 sec: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 770 ms: 1.20x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                                     |
| nbody          | 113 ms                                                                | 112 ms: 1.00x faster                                                     |
| float          | 89.6 ms                                                               | 91.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 129 ms: 1.06x faster                                                     |
| regex_dna      | 239 ms                                                                | 247 ms: 1.03x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 30.6 ms: 1.05x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.84 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                    |
| unpickle_pure_python | 278 us                                                                | 253 us: 1.10x faster                                                     |
| xml_etree_parse      | 209 ms                                                                | 191 ms: 1.10x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.45 us: 1.06x faster                                                    |
| pickle_pure_python   | 374 us                                                                | 363 us: 1.03x faster                                                     |
| tomli_loads          | 2.62 sec                                                              | 2.58 sec: 1.01x faster                                                   |
| pickle_dict          | 37.6 us                                                               | 38.0 us: 1.01x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.0 us: 1.06x slower                                                    |
| pickle_list          | 5.01 us                                                               | 5.35 us: 1.07x slower                                                    |
| pickle               | 12.8 us                                                               | 13.7 us: 1.07x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 82.1 ms: 1.08x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.64 ms: 1.18x slower                                                    |
| python_startup         | 10.2 ms                                                               | 13.0 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 62.2 ms                                                               | 60.4 ms: 1.03x faster                                                    |
| genshi_text     | 28.2 ms                                                               | 27.9 ms: 1.01x faster                                                    |
| django_template | 41.8 ms                                                               | 41.5 ms: 1.01x faster                                                    |
| mako            | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240603-arminc-aarch64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 197 us: 3.31x faster                                                     |
| generators                 | 64.2 ms                                                               | 37.4 ms: 1.72x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 590 ms: 1.56x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.20 sec: 1.45x faster                                                   |
| comprehensions             | 29.0 us                                                               | 20.2 us: 1.44x faster                                                    |
| async_tree_none            | 701 ms                                                                | 491 ms: 1.43x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 648 ms: 1.35x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.21 sec: 1.32x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 481 ms: 1.29x faster                                                     |
| deltablue                  | 4.75 ms                                                               | 3.88 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 787 ms: 1.21x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.28 sec: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 770 ms: 1.20x faster                                                     |
| pylint                     | 397 ms                                                                | 337 ms: 1.18x faster                                                     |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                                     |
| sympy_sum                  | 168 ms                                                                | 144 ms: 1.17x faster                                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.41 ms: 1.17x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                    |
| chaos                      | 78.8 ms                                                               | 68.2 ms: 1.16x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.73 ms: 1.15x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 29.2 ms: 1.14x faster                                                    |
| richards_super             | 70.2 ms                                                               | 62.3 ms: 1.13x faster                                                    |
| sympy_integrate            | 23.2 ms                                                               | 21.0 ms: 1.10x faster                                                    |
| sympy_str                  | 295 ms                                                                | 267 ms: 1.10x faster                                                     |
| unpickle_pure_python       | 278 us                                                                | 253 us: 1.10x faster                                                     |
| xml_etree_parse            | 209 ms                                                                | 191 ms: 1.10x faster                                                     |
| tornado_http               | 140 ms                                                                | 127 ms: 1.09x faster                                                     |
| dulwich_log                | 63.2 ms                                                               | 58.2 ms: 1.09x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.26 ms: 1.07x faster                                                    |
| logging_simple             | 7.57 us                                                               | 7.06 us: 1.07x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.45 us: 1.06x faster                                                    |
| regex_compile              | 137 ms                                                                | 129 ms: 1.06x faster                                                     |
| logging_format             | 8.22 us                                                               | 7.75 us: 1.06x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 23.5 ms: 1.06x faster                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 82.0 ms: 1.06x faster                                                    |
| hexiom                     | 7.57 ms                                                               | 7.20 ms: 1.05x faster                                                    |
| bench_mp_pool              | 7.44 ms                                                               | 7.11 ms: 1.05x faster                                                    |
| sympy_expand               | 482 ms                                                                | 463 ms: 1.04x faster                                                     |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                                     |
| dask                       | 385 ms                                                                | 373 ms: 1.03x faster                                                     |
| pickle_pure_python         | 374 us                                                                | 363 us: 1.03x faster                                                     |
| genshi_xml                 | 62.2 ms                                                               | 60.4 ms: 1.03x faster                                                    |
| nqueens                    | 102 ms                                                                | 99.6 ms: 1.03x faster                                                    |
| richards                   | 58.1 ms                                                               | 56.5 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 132 ms                                                                | 129 ms: 1.03x faster                                                     |
| sqlglot_optimize           | 63.4 ms                                                               | 62.4 ms: 1.02x faster                                                    |
| go                         | 163 ms                                                                | 161 ms: 1.01x faster                                                     |
| tomli_loads                | 2.62 sec                                                              | 2.58 sec: 1.01x faster                                                   |
| meteor_contest             | 115 ms                                                                | 114 ms: 1.01x faster                                                     |
| genshi_text                | 28.2 ms                                                               | 27.9 ms: 1.01x faster                                                    |
| django_template            | 41.8 ms                                                               | 41.5 ms: 1.01x faster                                                    |
| mako                       | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                                    |
| mdp                        | 3.35 sec                                                              | 3.33 sec: 1.01x faster                                                   |
| nbody                      | 113 ms                                                                | 112 ms: 1.00x faster                                                     |
| logging_silent             | 133 ns                                                                | 134 ns: 1.01x slower                                                     |
| scimark_lu                 | 140 ms                                                                | 142 ms: 1.01x slower                                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 84.2 ms: 1.01x slower                                                    |
| pickle_dict                | 37.6 us                                                               | 38.0 us: 1.01x slower                                                    |
| 2to3                       | 300 ms                                                                | 305 ms: 1.02x slower                                                     |
| json                       | 5.52 ms                                                               | 5.65 ms: 1.02x slower                                                    |
| float                      | 89.6 ms                                                               | 91.9 ms: 1.03x slower                                                    |
| pprint_pformat             | 1.85 sec                                                              | 1.91 sec: 1.03x slower                                                   |
| regex_dna                  | 239 ms                                                                | 247 ms: 1.03x slower                                                     |
| html5lib                   | 65.3 ms                                                               | 67.4 ms: 1.03x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 935 ms: 1.04x slower                                                     |
| deepcopy                   | 435 us                                                                | 452 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.53 ms: 1.04x slower                                                    |
| mypy2                      | 737 ms                                                                | 770 ms: 1.05x slower                                                     |
| aiohttp                    | 1.13 ms                                                               | 1.19 ms: 1.05x slower                                                    |
| regex_v8                   | 29.1 ms                                                               | 30.6 ms: 1.05x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.08 sec: 1.06x slower                                                   |
| json_loads                 | 30.3 us                                                               | 32.0 us: 1.06x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.12 us: 1.06x slower                                                    |
| thrift                     | 910 us                                                                | 964 us: 1.06x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 52.0 us: 1.06x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.35 us: 1.07x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.7 us: 1.07x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 8.89 ms: 1.07x slower                                                    |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.08x slower                                                     |
| xml_etree_process          | 76.1 ms                                                               | 82.1 ms: 1.08x slower                                                    |
| pyflate                    | 516 ms                                                                | 559 ms: 1.08x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| sqlite_synth               | 3.56 us                                                               | 3.91 us: 1.10x slower                                                    |
| scimark_sor                | 145 ms                                                                | 161 ms: 1.11x slower                                                     |
| scimark_fft                | 402 ms                                                                | 448 ms: 1.11x slower                                                     |
| flaskblogging              | 4.19 ms                                                               | 4.76 ms: 1.13x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.84 ms: 1.14x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.07 ms: 1.17x slower                                                    |
| coverage                   | 84.1 ms                                                               | 98.9 ms: 1.18x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.64 ms: 1.18x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.37 ms: 1.27x slower                                                    |
| python_startup             | 10.2 ms                                                               | 13.0 ms: 1.28x slower                                                    |
| telco                      | 7.80 ms                                                               | 10.0 ms: 1.29x slower                                                    |
| async_generators           | 378 ms                                                                | 487 ms: 1.29x slower                                                     |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                             |

Benchmark hidden because not significant (5): xml_etree_iterparse, fannkuch, gunicorn, pycparser, asyncio_websockets
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.11% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
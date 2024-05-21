# Results vs. 3.11.0

- fork: saulshanabrook
- ref: optimzer_type_versio
- machine: linux-x86_64
- commit hash: 1520928
- commit date: 2024-05-20
- overall geometric mean: 1.06x faster
- HPT reliability: 96.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                         |
| docutils       | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                        |
| html5lib       | 64.8 ms                                                | 68.4 ms: 1.05x slower                                                         |
| tornado_http   | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                          |
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 941 ms: 1.37x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 951 ms: 1.36x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 588 ms: 1.30x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.22x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.3 ms: 1.18x faster                                                         |
| float          | 78.9 ms                                                | 72.4 ms: 1.09x faster                                                         |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                          |
| regex_effbot   | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                         |
| regex_v8       | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                         |
| regex_dna      | 205 ms                                                 | 226 ms: 1.11x slower                                                          |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                         |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.17x faster                                                        |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.08x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 295 us: 1.08x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 153 ms: 1.07x faster                                                          |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| unpickle_list        | 5.21 us                                                | 5.33 us: 1.02x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 83.0 ms: 1.02x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 58.4 ms: 1.03x slower                                                         |
| pickle_dict          | 34.6 us                                                | 36.1 us: 1.04x slower                                                         |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                         |
| pickle_list          | 4.59 us                                                | 5.38 us: 1.17x slower                                                         |
| unpickle             | 13.8 us                                                | 16.7 us: 1.20x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                         |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.28x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.99 ms: 1.07x faster                                                         |
| genshi_xml      | 53.4 ms                                                | 58.1 ms: 1.09x slower                                                         |
| django_template | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                         |
| genshi_text     | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 170 us: 3.06x faster                                                          |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                        |
| asyncio_tcp                | 875 ms                                                 | 526 ms: 1.66x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                          |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.41x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                          |
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 941 ms: 1.37x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 951 ms: 1.36x faster                                                          |
| pylint                     | 476 ms                                                 | 355 ms: 1.34x faster                                                          |
| richards_super             | 61.9 ms                                                | 47.5 ms: 1.30x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 588 ms: 1.30x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.22x faster                                                          |
| richards                   | 49.8 ms                                                | 41.3 ms: 1.21x faster                                                         |
| chaos                      | 71.9 ms                                                | 60.1 ms: 1.20x faster                                                         |
| nbody                      | 96.0 ms                                                | 81.3 ms: 1.18x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.17x faster                                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 62.7 ms: 1.13x faster                                                         |
| coroutines                 | 27.0 ms                                                | 24.0 ms: 1.13x faster                                                         |
| fannkuch                   | 405 ms                                                 | 361 ms: 1.12x faster                                                          |
| pathlib                    | 18.5 ms                                                | 16.5 ms: 1.12x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 68.5 ms: 1.12x faster                                                         |
| raytrace                   | 309 ms                                                 | 278 ms: 1.11x faster                                                          |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.54 ms: 1.11x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.65 us: 1.10x faster                                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                         |
| float                      | 78.9 ms                                                | 72.4 ms: 1.09x faster                                                         |
| scimark_fft                | 345 ms                                                 | 318 ms: 1.09x faster                                                          |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.08x faster                                                          |
| pickle_pure_python         | 320 us                                                 | 295 us: 1.08x faster                                                          |
| spectral_norm              | 108 ms                                                 | 100 ms: 1.08x faster                                                          |
| logging_format             | 6.81 us                                                | 6.31 us: 1.08x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 153 ms: 1.07x faster                                                          |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                                        |
| mako                       | 10.7 ms                                                | 9.99 ms: 1.07x faster                                                         |
| deepcopy_memo              | 40.2 us                                                | 37.7 us: 1.07x faster                                                         |
| pprint_safe_repr           | 747 ms                                                 | 701 ms: 1.07x faster                                                          |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                         |
| deltablue                  | 3.92 ms                                                | 3.75 ms: 1.04x faster                                                         |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                          |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                          |
| nqueens                    | 87.9 ms                                                | 85.9 ms: 1.02x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.92 ms: 1.02x faster                                                         |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                          |
| tornado_http               | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                         |
| deepcopy                   | 365 us                                                 | 364 us: 1.00x faster                                                          |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                                          |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.28 us: 1.02x slower                                                         |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                        |
| sympy_str                  | 297 ms                                                 | 303 ms: 1.02x slower                                                          |
| unpickle_list              | 5.21 us                                                | 5.33 us: 1.02x slower                                                         |
| xml_etree_generate         | 81.1 ms                                                | 83.0 ms: 1.02x slower                                                         |
| xml_etree_process          | 56.9 ms                                                | 58.4 ms: 1.03x slower                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 57.0 ms: 1.03x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                          |
| bench_thread_pool          | 834 us                                                 | 865 us: 1.04x slower                                                          |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                          |
| dask                       | 365 ms                                                 | 380 ms: 1.04x slower                                                          |
| pickle_dict                | 34.6 us                                                | 36.1 us: 1.04x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                         |
| chameleon                  | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                         |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                                         |
| html5lib                   | 64.8 ms                                                | 68.4 ms: 1.05x slower                                                         |
| sympy_expand               | 484 ms                                                 | 512 ms: 1.06x slower                                                          |
| scimark_lu                 | 116 ms                                                 | 123 ms: 1.06x slower                                                          |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                          |
| dulwich_log                | 64.6 ms                                                | 69.5 ms: 1.08x slower                                                         |
| pyflate                    | 434 ms                                                 | 470 ms: 1.08x slower                                                          |
| genshi_xml                 | 53.4 ms                                                | 58.1 ms: 1.09x slower                                                         |
| django_template            | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                         |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                         |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                         |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.11x slower                                                          |
| docutils                   | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                        |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.12x slower                                                         |
| scimark_sor                | 121 ms                                                 | 137 ms: 1.13x slower                                                          |
| pickle_list                | 4.59 us                                                | 5.38 us: 1.17x slower                                                         |
| coverage                   | 78.8 ms                                                | 93.4 ms: 1.19x slower                                                         |
| telco                      | 6.86 ms                                                | 8.23 ms: 1.20x slower                                                         |
| unpickle                   | 13.8 us                                                | 16.7 us: 1.20x slower                                                         |
| async_generators           | 374 ms                                                 | 461 ms: 1.23x slower                                                          |
| flaskblogging              | 7.28 ms                                                | 9.22 ms: 1.27x slower                                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.28x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                  |

Benchmark hidden because not significant (4): json, go, meteor_contest, bench_mp_pool
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, hexiom, mdp, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x
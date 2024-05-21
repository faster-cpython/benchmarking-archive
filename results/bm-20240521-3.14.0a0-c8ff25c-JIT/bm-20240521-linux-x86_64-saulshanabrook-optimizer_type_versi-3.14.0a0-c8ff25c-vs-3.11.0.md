# Results vs. 3.11.0

- fork: saulshanabrook
- ref: optimizer_type_versi
- machine: linux-x86_64
- commit hash: c8ff25c
- commit date: 2024-05-21
- overall geometric mean: 1.07x faster
- HPT reliability: 96.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.05x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                         |
| docutils       | 2.66 sec                                               | 2.93 sec: 1.10x slower                                                        |
| html5lib       | 64.8 ms                                                | 66.3 ms: 1.02x slower                                                         |
| tornado_http   | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 330 ms: 1.49x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                                          |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 937 ms: 1.37x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 578 ms: 1.32x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.6 ms: 1.18x faster                                                         |
| float          | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                         |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.02x faster                                                          |
| regex_effbot   | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                         |
| regex_v8       | 22.9 ms                                                | 24.5 ms: 1.07x slower                                                         |
| regex_dna      | 205 ms                                                 | 231 ms: 1.13x slower                                                          |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                         |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                        |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                          |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                          |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| xml_etree_generate   | 81.1 ms                                                | 82.4 ms: 1.02x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 58.3 ms: 1.03x slower                                                         |
| unpickle_list        | 5.21 us                                                | 5.37 us: 1.03x slower                                                         |
| pickle_dict          | 34.6 us                                                | 36.3 us: 1.05x slower                                                         |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                         |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                                         |
| pickle_list          | 4.59 us                                                | 5.10 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                         |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                         |
| django_template | 33.5 ms                                                | 36.2 ms: 1.08x slower                                                         |
| genshi_xml      | 53.4 ms                                                | 58.0 ms: 1.09x slower                                                         |
| genshi_text     | 22.5 ms                                                | 24.9 ms: 1.10x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240521-linux-x86_64-saulshanabrook-optimizer_type_versi-3.14.0a0-c8ff25c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 172 us: 3.03x faster                                                          |
| generators                 | 74.9 ms                                                | 36.3 ms: 2.06x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 520 ms: 1.68x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                        |
| async_tree_none_tg         | 491 ms                                                 | 330 ms: 1.49x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                          |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                                          |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 937 ms: 1.37x faster                                                          |
| pylint                     | 476 ms                                                 | 354 ms: 1.35x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 578 ms: 1.32x faster                                                          |
| richards_super             | 61.9 ms                                                | 48.0 ms: 1.29x faster                                                         |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                          |
| richards                   | 49.8 ms                                                | 41.8 ms: 1.19x faster                                                         |
| chaos                      | 71.9 ms                                                | 60.5 ms: 1.19x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                        |
| coroutines                 | 27.0 ms                                                | 22.9 ms: 1.18x faster                                                         |
| nbody                      | 96.0 ms                                                | 81.6 ms: 1.18x faster                                                         |
| fannkuch                   | 405 ms                                                 | 356 ms: 1.14x faster                                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 62.1 ms: 1.14x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 67.8 ms: 1.13x faster                                                         |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.45 ms: 1.13x faster                                                         |
| pathlib                    | 18.5 ms                                                | 16.5 ms: 1.12x faster                                                         |
| raytrace                   | 309 ms                                                 | 280 ms: 1.10x faster                                                          |
| scimark_fft                | 345 ms                                                 | 313 ms: 1.10x faster                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.70 us: 1.09x faster                                                         |
| float                      | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                         |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                          |
| spectral_norm              | 108 ms                                                 | 100.0 ms: 1.08x faster                                                        |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                          |
| pprint_pformat             | 1.55 sec                                               | 1.44 sec: 1.08x faster                                                        |
| gc_traversal               | 4.01 ms                                                | 3.74 ms: 1.07x faster                                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                         |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| deepcopy_memo              | 40.2 us                                                | 37.7 us: 1.07x faster                                                         |
| logging_format             | 6.81 us                                                | 6.40 us: 1.06x faster                                                         |
| pprint_safe_repr           | 747 ms                                                 | 702 ms: 1.06x faster                                                          |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                          |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                         |
| deltablue                  | 3.92 ms                                                | 3.75 ms: 1.05x faster                                                         |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                          |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                          |
| nqueens                    | 87.9 ms                                                | 85.5 ms: 1.03x faster                                                         |
| regex_compile              | 141 ms                                                 | 138 ms: 1.02x faster                                                          |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                        |
| tornado_http               | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                         |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                          |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                          |
| sympy_str                  | 297 ms                                                 | 302 ms: 1.01x slower                                                          |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.01x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 82.4 ms: 1.02x slower                                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.29 us: 1.02x slower                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 56.6 ms: 1.02x slower                                                         |
| html5lib                   | 64.8 ms                                                | 66.3 ms: 1.02x slower                                                         |
| xml_etree_process          | 56.9 ms                                                | 58.3 ms: 1.03x slower                                                         |
| deepcopy                   | 365 us                                                 | 375 us: 1.03x slower                                                          |
| dask                       | 365 ms                                                 | 375 ms: 1.03x slower                                                          |
| unpickle_list              | 5.21 us                                                | 5.37 us: 1.03x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                          |
| bench_thread_pool          | 834 us                                                 | 866 us: 1.04x slower                                                          |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                          |
| pyflate                    | 434 ms                                                 | 453 ms: 1.04x slower                                                          |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                         |
| pickle_dict                | 34.6 us                                                | 36.3 us: 1.05x slower                                                         |
| sympy_expand               | 484 ms                                                 | 509 ms: 1.05x slower                                                          |
| chameleon                  | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                         |
| 2to3                       | 264 ms                                                 | 278 ms: 1.05x slower                                                          |
| scimark_lu                 | 116 ms                                                 | 123 ms: 1.06x slower                                                          |
| regex_effbot               | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                         |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 24.5 ms: 1.07x slower                                                         |
| dulwich_log                | 64.6 ms                                                | 69.3 ms: 1.07x slower                                                         |
| django_template            | 33.5 ms                                                | 36.2 ms: 1.08x slower                                                         |
| genshi_xml                 | 53.4 ms                                                | 58.0 ms: 1.09x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 2.83 us: 1.10x slower                                                         |
| docutils                   | 2.66 sec                                               | 2.93 sec: 1.10x slower                                                        |
| genshi_text                | 22.5 ms                                                | 24.9 ms: 1.10x slower                                                         |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                                         |
| pickle_list                | 4.59 us                                                | 5.10 us: 1.11x slower                                                         |
| regex_dna                  | 205 ms                                                 | 231 ms: 1.13x slower                                                          |
| scimark_sor                | 121 ms                                                 | 138 ms: 1.13x slower                                                          |
| coverage                   | 78.8 ms                                                | 93.0 ms: 1.18x slower                                                         |
| telco                      | 6.86 ms                                                | 8.22 ms: 1.20x slower                                                         |
| async_generators           | 374 ms                                                 | 463 ms: 1.24x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                         |
| flaskblogging              | 7.28 ms                                                | 9.23 ms: 1.27x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                  |

Benchmark hidden because not significant (3): json, bench_mp_pool, go
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, hexiom, mdp, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.86% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x
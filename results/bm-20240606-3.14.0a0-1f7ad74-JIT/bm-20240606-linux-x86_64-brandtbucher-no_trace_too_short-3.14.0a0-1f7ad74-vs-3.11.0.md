# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_trace_too_short
- machine: linux-x86_64
- commit hash: 1f7ad74
- commit date: 2024-06-06
- overall geometric mean: 1.06x faster
- HPT reliability: 98.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                      |
| docutils       | 2.66 sec                                               | 2.97 sec: 1.11x slower                                                    |
| html5lib       | 64.8 ms                                                | 69.5 ms: 1.07x slower                                                     |
| tornado_http   | 98.1 ms                                                | 96.8 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                  | 1.06x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                      |
| async_tree_io_tg           | 1.29 sec                                               | 916 ms: 1.41x faster                                                      |
| async_tree_none            | 528 ms                                                 | 376 ms: 1.40x faster                                                      |
| async_tree_io              | 1.29 sec                                               | 963 ms: 1.34x faster                                                      |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.34x faster                                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.8 ms: 1.17x faster                                                     |
| float          | 78.9 ms                                                | 73.0 ms: 1.08x faster                                                     |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                  | 1.09x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.02x faster                                                      |
| regex_effbot   | 3.51 ms                                                | 4.01 ms: 1.14x slower                                                     |
| regex_v8       | 22.9 ms                                                | 26.6 ms: 1.16x slower                                                     |
| regex_dna      | 205 ms                                                 | 238 ms: 1.16x slower                                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                     |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                      |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.09x faster                                                      |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                      |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                      |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                     |
| xml_etree_generate   | 81.1 ms                                                | 81.3 ms: 1.00x slower                                                     |
| pickle_dict          | 34.6 us                                                | 35.2 us: 1.02x slower                                                     |
| xml_etree_process    | 56.9 ms                                                | 58.3 ms: 1.02x slower                                                     |
| unpickle_list        | 5.21 us                                                | 5.43 us: 1.04x slower                                                     |
| unpickle             | 13.8 us                                                | 14.9 us: 1.08x slower                                                     |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                     |
| pickle_list          | 4.59 us                                                | 5.05 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.62 ms: 1.27x slower                                                     |
| python_startup         | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.0 ms: 1.07x faster                                                     |
| genshi_xml      | 53.4 ms                                                | 58.1 ms: 1.09x slower                                                     |
| django_template | 33.5 ms                                                | 36.8 ms: 1.10x slower                                                     |
| genshi_text     | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-no_trace_too_short-3.14.0a0-1f7ad74 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 170 us: 3.05x faster                                                      |
| generators                 | 74.9 ms                                                | 30.5 ms: 2.45x faster                                                     |
| asyncio_tcp                | 875 ms                                                 | 517 ms: 1.69x faster                                                      |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                      |
| async_tree_io_tg           | 1.29 sec                                               | 916 ms: 1.41x faster                                                      |
| async_tree_none            | 528 ms                                                 | 376 ms: 1.40x faster                                                      |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                     |
| pylint                     | 476 ms                                                 | 354 ms: 1.34x faster                                                      |
| async_tree_io              | 1.29 sec                                               | 963 ms: 1.34x faster                                                      |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.34x faster                                                      |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                                      |
| richards_super             | 61.9 ms                                                | 49.2 ms: 1.26x faster                                                     |
| chaos                      | 71.9 ms                                                | 59.4 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                      |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                    |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.18x faster                                                     |
| nbody                      | 96.0 ms                                                | 81.8 ms: 1.17x faster                                                     |
| richards                   | 49.8 ms                                                | 42.5 ms: 1.17x faster                                                     |
| fannkuch                   | 405 ms                                                 | 350 ms: 1.16x faster                                                      |
| crypto_pyaes               | 76.7 ms                                                | 67.9 ms: 1.13x faster                                                     |
| scimark_monte_carlo        | 70.7 ms                                                | 62.6 ms: 1.13x faster                                                     |
| pathlib                    | 18.5 ms                                                | 16.6 ms: 1.12x faster                                                     |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.55 ms: 1.10x faster                                                     |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                      |
| logging_simple             | 6.22 us                                                | 5.66 us: 1.10x faster                                                     |
| scimark_fft                | 345 ms                                                 | 318 ms: 1.09x faster                                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                     |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.09x faster                                                      |
| float                      | 78.9 ms                                                | 73.0 ms: 1.08x faster                                                     |
| logging_format             | 6.81 us                                                | 6.31 us: 1.08x faster                                                     |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.08x faster                                                    |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                      |
| mako                       | 10.7 ms                                                | 10.0 ms: 1.07x faster                                                     |
| spectral_norm              | 108 ms                                                 | 102 ms: 1.06x faster                                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.06x faster                                                     |
| deepcopy_memo              | 40.2 us                                                | 38.1 us: 1.05x faster                                                     |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                      |
| gc_traversal               | 4.01 ms                                                | 3.83 ms: 1.05x faster                                                     |
| hexiom                     | 6.89 ms                                                | 6.59 ms: 1.05x faster                                                     |
| pprint_pformat             | 1.55 sec                                               | 1.49 sec: 1.04x faster                                                    |
| pprint_safe_repr           | 747 ms                                                 | 724 ms: 1.03x faster                                                      |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                      |
| deltablue                  | 3.92 ms                                                | 3.82 ms: 1.03x faster                                                     |
| nqueens                    | 87.9 ms                                                | 85.7 ms: 1.02x faster                                                     |
| logging_silent             | 111 ns                                                 | 108 ns: 1.02x faster                                                      |
| regex_compile              | 141 ms                                                 | 138 ms: 1.02x faster                                                      |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                     |
| tornado_http               | 98.1 ms                                                | 96.8 ms: 1.01x faster                                                     |
| go                         | 149 ms                                                 | 148 ms: 1.01x faster                                                      |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                      |
| xml_etree_generate         | 81.1 ms                                                | 81.3 ms: 1.00x slower                                                     |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                      |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                                      |
| pickle_dict                | 34.6 us                                                | 35.2 us: 1.02x slower                                                     |
| sympy_str                  | 297 ms                                                 | 303 ms: 1.02x slower                                                      |
| deepcopy                   | 365 us                                                 | 373 us: 1.02x slower                                                      |
| xml_etree_process          | 56.9 ms                                                | 58.3 ms: 1.02x slower                                                     |
| json                       | 5.24 ms                                                | 5.38 ms: 1.03x slower                                                     |
| pyflate                    | 434 ms                                                 | 446 ms: 1.03x slower                                                      |
| pycparser                  | 1.19 sec                                               | 1.22 sec: 1.03x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 57.0 ms: 1.03x slower                                                     |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                      |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                      |
| unpickle_list              | 5.21 us                                                | 5.43 us: 1.04x slower                                                     |
| thrift                     | 784 us                                                 | 818 us: 1.04x slower                                                      |
| deepcopy_reduce            | 3.22 us                                                | 3.36 us: 1.04x slower                                                     |
| bench_thread_pool          | 834 us                                                 | 882 us: 1.06x slower                                                      |
| dulwich_log                | 64.6 ms                                                | 68.3 ms: 1.06x slower                                                     |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                      |
| sympy_integrate            | 21.5 ms                                                | 22.7 ms: 1.06x slower                                                     |
| sympy_expand               | 484 ms                                                 | 515 ms: 1.06x slower                                                      |
| html5lib                   | 64.8 ms                                                | 69.5 ms: 1.07x slower                                                     |
| unpickle                   | 13.8 us                                                | 14.9 us: 1.08x slower                                                     |
| scimark_lu                 | 116 ms                                                 | 126 ms: 1.08x slower                                                      |
| genshi_xml                 | 53.4 ms                                                | 58.1 ms: 1.09x slower                                                     |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                     |
| django_template            | 33.5 ms                                                | 36.8 ms: 1.10x slower                                                     |
| pickle_list                | 4.59 us                                                | 5.05 us: 1.10x slower                                                     |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.10x slower                                                     |
| genshi_text                | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                     |
| docutils                   | 2.66 sec                                               | 2.97 sec: 1.11x slower                                                    |
| scimark_sor                | 121 ms                                                 | 138 ms: 1.14x slower                                                      |
| regex_effbot               | 3.51 ms                                                | 4.01 ms: 1.14x slower                                                     |
| regex_v8                   | 22.9 ms                                                | 26.6 ms: 1.16x slower                                                     |
| regex_dna                  | 205 ms                                                 | 238 ms: 1.16x slower                                                      |
| telco                      | 6.86 ms                                                | 8.06 ms: 1.18x slower                                                     |
| coverage                   | 78.8 ms                                                | 93.8 ms: 1.19x slower                                                     |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.81 ms: 1.26x slower                                                     |
| python_startup_no_site     | 6.01 ms                                                | 7.62 ms: 1.27x slower                                                     |
| python_startup             | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                              |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.15% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
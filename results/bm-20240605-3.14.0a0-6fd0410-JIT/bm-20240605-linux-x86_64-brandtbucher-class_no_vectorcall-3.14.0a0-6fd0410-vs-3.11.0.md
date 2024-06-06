# Results vs. 3.11.0

- fork: brandtbucher
- ref: class_no_vectorcall
- machine: linux-x86_64
- commit hash: 6fd0410
- commit date: 2024-06-05
- overall geometric mean: 1.07x faster
- HPT reliability: 98.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.05x slower                                                       |
| docutils       | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                     |
| html5lib       | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 339 ms: 1.45x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                       |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.39x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 954 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 595 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.19x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.6 ms: 1.19x faster                                                      |
| float          | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                      |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                  | 1.10x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.03x faster                                                       |
| regex_effbot   | 3.51 ms                                                | 3.81 ms: 1.09x slower                                                      |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                                       |
| regex_v8       | 22.9 ms                                                | 26.1 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                  | 1.08x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                      |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.18x faster                                                     |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                       |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                       |
| pickle_pure_python   | 320 us                                                 | 297 us: 1.08x faster                                                       |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                       |
| xml_etree_process    | 56.9 ms                                                | 57.7 ms: 1.01x slower                                                      |
| pickle_dict          | 34.6 us                                                | 35.9 us: 1.04x slower                                                      |
| unpickle_list        | 5.21 us                                                | 5.46 us: 1.05x slower                                                      |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                      |
| unpickle             | 13.8 us                                                | 15.9 us: 1.15x slower                                                      |
| pickle_list          | 4.59 us                                                | 5.29 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.61 ms: 1.27x slower                                                      |
| python_startup         | 8.56 ms                                                | 11.2 ms: 1.30x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.98 ms: 1.07x faster                                                      |
| genshi_xml      | 53.4 ms                                                | 57.0 ms: 1.07x slower                                                      |
| django_template | 33.5 ms                                                | 36.8 ms: 1.10x slower                                                      |
| genshi_text     | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-class_no_vectorcall-3.14.0a0-6fd0410 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                                       |
| generators                 | 74.9 ms                                                | 30.7 ms: 2.44x faster                                                      |
| asyncio_tcp                | 875 ms                                                 | 521 ms: 1.68x faster                                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 339 ms: 1.45x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                       |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                      |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.39x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                       |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 954 ms: 1.35x faster                                                       |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                      |
| richards_super             | 61.9 ms                                                | 47.9 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 595 ms: 1.28x faster                                                       |
| richards                   | 49.8 ms                                                | 41.5 ms: 1.20x faster                                                      |
| nbody                      | 96.0 ms                                                | 80.6 ms: 1.19x faster                                                      |
| chaos                      | 71.9 ms                                                | 60.3 ms: 1.19x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.19x faster                                                       |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.18x faster                                                     |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.43 ms: 1.13x faster                                                      |
| pathlib                    | 18.5 ms                                                | 16.4 ms: 1.13x faster                                                      |
| fannkuch                   | 405 ms                                                 | 361 ms: 1.12x faster                                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 63.0 ms: 1.12x faster                                                      |
| crypto_pyaes               | 76.7 ms                                                | 68.4 ms: 1.12x faster                                                      |
| logging_simple             | 6.22 us                                                | 5.61 us: 1.11x faster                                                      |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                       |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                       |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                      |
| gc_traversal               | 4.01 ms                                                | 3.66 ms: 1.10x faster                                                      |
| float                      | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                      |
| scimark_fft                | 345 ms                                                 | 318 ms: 1.09x faster                                                       |
| logging_format             | 6.81 us                                                | 6.29 us: 1.08x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 297 us: 1.08x faster                                                       |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                       |
| mako                       | 10.7 ms                                                | 9.98 ms: 1.07x faster                                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                      |
| spectral_norm              | 108 ms                                                 | 102 ms: 1.06x faster                                                       |
| deepcopy_memo              | 40.2 us                                                | 38.1 us: 1.05x faster                                                      |
| deltablue                  | 3.92 ms                                                | 3.73 ms: 1.05x faster                                                      |
| pprint_pformat             | 1.55 sec                                               | 1.48 sec: 1.05x faster                                                     |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                       |
| hexiom                     | 6.89 ms                                                | 6.59 ms: 1.05x faster                                                      |
| pprint_safe_repr           | 747 ms                                                 | 723 ms: 1.03x faster                                                       |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                       |
| regex_compile              | 141 ms                                                 | 138 ms: 1.03x faster                                                       |
| nqueens                    | 87.9 ms                                                | 85.7 ms: 1.02x faster                                                      |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                       |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                       |
| mdp                        | 2.77 sec                                               | 2.77 sec: 1.00x faster                                                     |
| sympy_str                  | 297 ms                                                 | 300 ms: 1.01x slower                                                       |
| xml_etree_process          | 56.9 ms                                                | 57.7 ms: 1.01x slower                                                      |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                                      |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                                       |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                     |
| sqlglot_optimize           | 55.3 ms                                                | 56.6 ms: 1.02x slower                                                      |
| deepcopy                   | 365 us                                                 | 374 us: 1.02x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                       |
| json                       | 5.24 ms                                                | 5.43 ms: 1.04x slower                                                      |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                       |
| pickle_dict                | 34.6 us                                                | 35.9 us: 1.04x slower                                                      |
| sympy_expand               | 484 ms                                                 | 506 ms: 1.04x slower                                                       |
| html5lib                   | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                      |
| unpickle_list              | 5.21 us                                                | 5.46 us: 1.05x slower                                                      |
| pyflate                    | 434 ms                                                 | 454 ms: 1.05x slower                                                       |
| thrift                     | 784 us                                                 | 822 us: 1.05x slower                                                       |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                      |
| bench_thread_pool          | 834 us                                                 | 877 us: 1.05x slower                                                       |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.05x slower                                                       |
| 2to3                       | 264 ms                                                 | 279 ms: 1.05x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 57.0 ms: 1.07x slower                                                      |
| scimark_lu                 | 116 ms                                                 | 124 ms: 1.07x slower                                                       |
| dulwich_log                | 64.6 ms                                                | 69.7 ms: 1.08x slower                                                      |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                      |
| regex_effbot               | 3.51 ms                                                | 3.81 ms: 1.09x slower                                                      |
| django_template            | 33.5 ms                                                | 36.8 ms: 1.10x slower                                                      |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                      |
| docutils                   | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                     |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                      |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                                       |
| regex_v8                   | 22.9 ms                                                | 26.1 ms: 1.14x slower                                                      |
| unpickle                   | 13.8 us                                                | 15.9 us: 1.15x slower                                                      |
| pickle_list                | 4.59 us                                                | 5.29 us: 1.15x slower                                                      |
| telco                      | 6.86 ms                                                | 8.04 ms: 1.17x slower                                                      |
| coverage                   | 78.8 ms                                                | 94.2 ms: 1.20x slower                                                      |
| async_generators           | 374 ms                                                 | 464 ms: 1.24x slower                                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                      |
| python_startup_no_site     | 6.01 ms                                                | 7.61 ms: 1.27x slower                                                      |
| python_startup             | 8.56 ms                                                | 11.2 ms: 1.30x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                               |

Benchmark hidden because not significant (5): tornado_http, json_loads, xml_etree_generate, bench_mp_pool, sqlglot_normalize
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.62% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
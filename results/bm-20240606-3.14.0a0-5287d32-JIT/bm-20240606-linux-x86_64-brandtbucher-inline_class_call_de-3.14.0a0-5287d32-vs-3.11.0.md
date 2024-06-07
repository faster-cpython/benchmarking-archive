# Results vs. 3.11.0

- fork: brandtbucher
- ref: inline_class_call_de
- machine: linux-x86_64
- commit hash: 5287d32
- commit date: 2024-06-06
- overall geometric mean: 1.07x faster
- HPT reliability: 98.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                        |
| docutils       | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                      |
| html5lib       | 64.8 ms                                                | 68.8 ms: 1.06x slower                                                       |
| tornado_http   | 98.1 ms                                                | 98.7 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.43x faster                                                        |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                        |
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 981 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 598 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                        |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.4 ms: 1.19x faster                                                       |
| float          | 78.9 ms                                                | 73.6 ms: 1.07x faster                                                       |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.02x faster                                                        |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                                        |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                       |
| regex_effbot   | 3.51 ms                                                | 4.00 ms: 1.14x slower                                                       |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                       |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                      |
| xml_etree_parse      | 164 ms                                                 | 148 ms: 1.11x faster                                                        |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                        |
| pickle_pure_python   | 320 us                                                 | 303 us: 1.05x faster                                                        |
| xml_etree_generate   | 81.1 ms                                                | 82.3 ms: 1.01x slower                                                       |
| xml_etree_process    | 56.9 ms                                                | 58.1 ms: 1.02x slower                                                       |
| pickle_dict          | 34.6 us                                                | 35.7 us: 1.03x slower                                                       |
| unpickle_list        | 5.21 us                                                | 5.41 us: 1.04x slower                                                       |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                       |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                       |
| pickle_list          | 4.59 us                                                | 5.24 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.64 ms: 1.27x slower                                                       |
| python_startup         | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                       |
| django_template | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                       |
| genshi_xml      | 53.4 ms                                                | 58.6 ms: 1.10x slower                                                       |
| genshi_text     | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-5287d32 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 171 us: 3.05x faster                                                        |
| generators                 | 74.9 ms                                                | 30.7 ms: 2.44x faster                                                       |
| asyncio_tcp                | 875 ms                                                 | 522 ms: 1.68x faster                                                        |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                      |
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.43x faster                                                        |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                        |
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                        |
| pylint                     | 476 ms                                                 | 354 ms: 1.34x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 981 ms: 1.31x faster                                                        |
| richards_super             | 61.9 ms                                                | 47.8 ms: 1.29x faster                                                       |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 598 ms: 1.27x faster                                                        |
| chaos                      | 71.9 ms                                                | 59.6 ms: 1.21x faster                                                       |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                       |
| richards                   | 49.8 ms                                                | 41.7 ms: 1.19x faster                                                       |
| nbody                      | 96.0 ms                                                | 80.4 ms: 1.19x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                        |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.39 ms: 1.15x faster                                                       |
| fannkuch                   | 405 ms                                                 | 354 ms: 1.15x faster                                                        |
| crypto_pyaes               | 76.7 ms                                                | 67.5 ms: 1.14x faster                                                       |
| pathlib                    | 18.5 ms                                                | 16.4 ms: 1.13x faster                                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 62.7 ms: 1.13x faster                                                       |
| xml_etree_parse            | 164 ms                                                 | 148 ms: 1.11x faster                                                        |
| logging_simple             | 6.22 us                                                | 5.62 us: 1.11x faster                                                       |
| raytrace                   | 309 ms                                                 | 279 ms: 1.10x faster                                                        |
| scimark_fft                | 345 ms                                                 | 315 ms: 1.10x faster                                                        |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                        |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                       |
| logging_format             | 6.81 us                                                | 6.30 us: 1.08x faster                                                       |
| spectral_norm              | 108 ms                                                 | 100 ms: 1.08x faster                                                        |
| pprint_pformat             | 1.55 sec                                               | 1.44 sec: 1.08x faster                                                      |
| float                      | 78.9 ms                                                | 73.6 ms: 1.07x faster                                                       |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                        |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                       |
| deltablue                  | 3.92 ms                                                | 3.71 ms: 1.06x faster                                                       |
| pickle_pure_python         | 320 us                                                 | 303 us: 1.05x faster                                                        |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                       |
| pprint_safe_repr           | 747 ms                                                 | 711 ms: 1.05x faster                                                        |
| mdp                        | 2.77 sec                                               | 2.65 sec: 1.05x faster                                                      |
| deepcopy_memo              | 40.2 us                                                | 38.8 us: 1.04x faster                                                       |
| hexiom                     | 6.89 ms                                                | 6.67 ms: 1.03x faster                                                       |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                        |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                        |
| regex_compile              | 141 ms                                                 | 139 ms: 1.02x faster                                                        |
| gc_traversal               | 4.01 ms                                                | 3.94 ms: 1.02x faster                                                       |
| nqueens                    | 87.9 ms                                                | 86.6 ms: 1.01x faster                                                       |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                        |
| go                         | 149 ms                                                 | 148 ms: 1.01x faster                                                        |
| tornado_http               | 98.1 ms                                                | 98.7 ms: 1.01x slower                                                       |
| pyflate                    | 434 ms                                                 | 439 ms: 1.01x slower                                                        |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                        |
| xml_etree_generate         | 81.1 ms                                                | 82.3 ms: 1.01x slower                                                       |
| xml_etree_process          | 56.9 ms                                                | 58.1 ms: 1.02x slower                                                       |
| sympy_str                  | 297 ms                                                 | 304 ms: 1.02x slower                                                        |
| deepcopy                   | 365 us                                                 | 374 us: 1.02x slower                                                        |
| pycparser                  | 1.19 sec                                               | 1.22 sec: 1.03x slower                                                      |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                                       |
| sympy_sum                  | 169 ms                                                 | 174 ms: 1.03x slower                                                        |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                        |
| pickle_dict                | 34.6 us                                                | 35.7 us: 1.03x slower                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 57.2 ms: 1.03x slower                                                       |
| unpickle_list              | 5.21 us                                                | 5.41 us: 1.04x slower                                                       |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                        |
| thrift                     | 784 us                                                 | 818 us: 1.04x slower                                                        |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                                       |
| sympy_expand               | 484 ms                                                 | 511 ms: 1.06x slower                                                        |
| bench_thread_pool          | 834 us                                                 | 883 us: 1.06x slower                                                        |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                        |
| html5lib                   | 64.8 ms                                                | 68.8 ms: 1.06x slower                                                       |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                                        |
| dulwich_log                | 64.6 ms                                                | 69.5 ms: 1.08x slower                                                       |
| django_template            | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                       |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 58.6 ms: 1.10x slower                                                       |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                        |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                       |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.11x slower                                                       |
| docutils                   | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                      |
| genshi_text                | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                       |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                                        |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                       |
| pickle_list                | 4.59 us                                                | 5.24 us: 1.14x slower                                                       |
| regex_effbot               | 3.51 ms                                                | 4.00 ms: 1.14x slower                                                       |
| telco                      | 6.86 ms                                                | 8.04 ms: 1.17x slower                                                       |
| coverage                   | 78.8 ms                                                | 93.6 ms: 1.19x slower                                                       |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                        |
| create_gc_cycles           | 1.43 ms                                                | 1.81 ms: 1.26x slower                                                       |
| python_startup_no_site     | 6.01 ms                                                | 7.64 ms: 1.27x slower                                                       |
| python_startup             | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                |

Benchmark hidden because not significant (2): json_loads, bench_mp_pool
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.02% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
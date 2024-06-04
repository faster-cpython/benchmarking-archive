# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: stackref_all
- machine: linux-x86_64
- commit hash: c73f8ac
- commit date: 2024-06-04
- overall geometric mean: 1.06x faster
- HPT reliability: 90.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                    |
| docutils       | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                  |
| html5lib       | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                   |
| tornado_http   | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 914 ms: 1.42x faster                                                    |
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.40x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 950 ms: 1.35x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 473 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.18x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.2 ms: 1.04x faster                                                   |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                    |
| regex_effbot   | 3.51 ms                                                | 3.70 ms: 1.05x slower                                                   |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                    |
| regex_v8       | 22.9 ms                                                | 24.9 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 227 us: 1.06x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.23 sec: 1.03x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 312 us: 1.02x faster                                                    |
| unpickle_list        | 5.21 us                                                | 5.25 us: 1.01x slower                                                   |
| pickle_dict          | 34.6 us                                                | 36.2 us: 1.05x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 87.5 ms: 1.08x slower                                                   |
| pickle               | 11.0 us                                                | 11.9 us: 1.09x slower                                                   |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.35 us: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (2): json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 53.9 ms: 1.01x slower                                                   |
| genshi_text     | 22.5 ms                                                | 23.3 ms: 1.04x slower                                                   |
| django_template | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                   |
| mako            | 10.7 ms                                                | 12.0 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 171 us: 3.04x faster                                                    |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                  |
| pylint                     | 476 ms                                                 | 317 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 914 ms: 1.42x faster                                                    |
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.40x faster                                                    |
| comprehensions             | 23.6 us                                                | 17.1 us: 1.38x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 950 ms: 1.35x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 473 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.18x faster                                                    |
| deltablue                  | 3.92 ms                                                | 3.35 ms: 1.17x faster                                                   |
| chaos                      | 71.9 ms                                                | 62.0 ms: 1.16x faster                                                   |
| raytrace                   | 309 ms                                                 | 269 ms: 1.15x faster                                                    |
| coroutines                 | 27.0 ms                                                | 23.7 ms: 1.14x faster                                                   |
| pathlib                    | 18.5 ms                                                | 16.3 ms: 1.14x faster                                                   |
| richards_super             | 61.9 ms                                                | 54.4 ms: 1.14x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                    |
| hexiom                     | 6.89 ms                                                | 6.38 ms: 1.08x faster                                                   |
| nqueens                    | 87.9 ms                                                | 82.1 ms: 1.07x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.34 ms: 1.07x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.84 us: 1.06x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 227 us: 1.06x faster                                                    |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.05x faster                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.05x faster                                                   |
| logging_format             | 6.81 us                                                | 6.48 us: 1.05x faster                                                   |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                   |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                    |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                    |
| nbody                      | 96.0 ms                                                | 92.2 ms: 1.04x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                    |
| tornado_http               | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                   |
| richards                   | 49.8 ms                                                | 48.2 ms: 1.03x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 2.23 sec: 1.03x faster                                                  |
| go                         | 149 ms                                                 | 145 ms: 1.02x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 312 us: 1.02x faster                                                    |
| sympy_expand               | 484 ms                                                 | 474 ms: 1.02x faster                                                    |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.02x faster                                                  |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.01x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 3.95 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 69.9 ms: 1.01x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                   |
| mdp                        | 2.77 sec                                               | 2.76 sec: 1.00x faster                                                  |
| bench_thread_pool          | 834 us                                                 | 838 us: 1.00x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 55.6 ms: 1.00x slower                                                   |
| unpickle_list              | 5.21 us                                                | 5.25 us: 1.01x slower                                                   |
| genshi_xml                 | 53.4 ms                                                | 53.9 ms: 1.01x slower                                                   |
| dask                       | 365 ms                                                 | 370 ms: 1.01x slower                                                    |
| scimark_lu                 | 116 ms                                                 | 118 ms: 1.01x slower                                                    |
| pprint_pformat             | 1.55 sec                                               | 1.58 sec: 1.02x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 66.0 ms: 1.02x slower                                                   |
| deepcopy_memo              | 40.2 us                                                | 41.0 us: 1.02x slower                                                   |
| deepcopy                   | 365 us                                                 | 373 us: 1.02x slower                                                    |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                    |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                                   |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                    |
| thrift                     | 784 us                                                 | 809 us: 1.03x slower                                                    |
| genshi_text                | 22.5 ms                                                | 23.3 ms: 1.04x slower                                                   |
| html5lib                   | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 780 ms: 1.04x slower                                                    |
| pickle_dict                | 34.6 us                                                | 36.2 us: 1.05x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.36 us: 1.05x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.70 ms: 1.05x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                   |
| django_template            | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                   |
| scimark_sor                | 121 ms                                                 | 131 ms: 1.08x slower                                                    |
| xml_etree_generate         | 81.1 ms                                                | 87.5 ms: 1.08x slower                                                   |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                    |
| pickle                     | 11.0 us                                                | 11.9 us: 1.09x slower                                                   |
| pyflate                    | 434 ms                                                 | 471 ms: 1.09x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 24.9 ms: 1.09x slower                                                   |
| scimark_fft                | 345 ms                                                 | 376 ms: 1.09x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                   |
| spectral_norm              | 108 ms                                                 | 118 ms: 1.09x slower                                                    |
| mako                       | 10.7 ms                                                | 12.0 ms: 1.12x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.35 us: 1.17x slower                                                   |
| coverage                   | 78.8 ms                                                | 92.5 ms: 1.17x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                   |
| async_generators           | 374 ms                                                 | 452 ms: 1.21x slower                                                    |
| telco                      | 6.86 ms                                                | 8.45 ms: 1.23x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.24x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (6): scimark_sparse_mat_mult, crypto_pyaes, json_loads, float, fannkuch, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 90.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
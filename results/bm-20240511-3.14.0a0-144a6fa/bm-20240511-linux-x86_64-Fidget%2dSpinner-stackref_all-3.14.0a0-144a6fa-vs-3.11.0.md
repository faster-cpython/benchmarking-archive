# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: stackref_all
- machine: linux-x86_64
- commit hash: 144a6fa
- commit date: 2024-05-11
- overall geometric mean: 1.02x slower
- HPT reliability: 97.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                    |
| chameleon      | 6.70 ms                                                | 7.80 ms: 1.16x slower                                                   |
| docutils       | 2.66 sec                                               | 2.89 sec: 1.08x slower                                                  |
| html5lib       | 64.8 ms                                                | 69.6 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 362 ms: 1.36x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 960 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 476 ms: 1.31x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 499 ms: 1.28x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 636 ms: 1.18x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| nbody          | 96.0 ms                                                | 105 ms: 1.09x slower                                                    |
| float          | 78.9 ms                                                | 86.7 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 144 ms: 1.02x slower                                                    |
| regex_effbot   | 3.51 ms                                                | 3.60 ms: 1.03x slower                                                   |
| regex_dna      | 205 ms                                                 | 217 ms: 1.06x slower                                                    |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                   |
| pickle_dict          | 34.6 us                                                | 33.9 us: 1.02x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 243 us: 1.01x slower                                                    |
| tomli_loads          | 2.30 sec                                               | 2.34 sec: 1.01x slower                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 112 ms: 1.03x slower                                                    |
| pickle_pure_python   | 320 us                                                 | 335 us: 1.05x slower                                                    |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                   |
| unpickle_list        | 5.21 us                                                | 5.55 us: 1.06x slower                                                   |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 65.1 ms: 1.14x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 93.4 ms: 1.15x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.41 us: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.16 ms: 1.19x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 55.7 ms: 1.04x slower                                                   |
| genshi_text     | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                   |
| django_template | 33.5 ms                                                | 38.2 ms: 1.14x slower                                                   |
| mako            | 10.7 ms                                                | 12.7 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.12x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-144a6fa |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 178 us: 2.91x faster                                                    |
| generators                 | 74.9 ms                                                | 31.3 ms: 2.39x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 516 ms: 1.70x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                  |
| pylint                     | 476 ms                                                 | 332 ms: 1.44x faster                                                    |
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 362 ms: 1.36x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 960 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 476 ms: 1.31x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 499 ms: 1.28x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                    |
| comprehensions             | 23.6 us                                                | 19.0 us: 1.24x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 636 ms: 1.18x faster                                                    |
| deltablue                  | 3.92 ms                                                | 3.60 ms: 1.09x faster                                                   |
| chaos                      | 71.9 ms                                                | 66.8 ms: 1.08x faster                                                   |
| raytrace                   | 309 ms                                                 | 289 ms: 1.07x faster                                                    |
| coroutines                 | 27.0 ms                                                | 25.5 ms: 1.06x faster                                                   |
| richards_super             | 61.9 ms                                                | 58.5 ms: 1.06x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.81 ms: 1.05x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 161 ms: 1.05x faster                                                    |
| mdp                        | 2.77 sec                                               | 2.66 sec: 1.04x faster                                                  |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.04x faster                                                   |
| logging_simple             | 6.22 us                                                | 6.06 us: 1.03x faster                                                   |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| sympy_str                  | 297 ms                                                 | 291 ms: 1.02x faster                                                    |
| pickle_dict                | 34.6 us                                                | 33.9 us: 1.02x faster                                                   |
| logging_format             | 6.81 us                                                | 6.72 us: 1.01x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.82 ms: 1.01x faster                                                   |
| sympy_integrate            | 21.5 ms                                                | 21.2 ms: 1.01x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 243 us: 1.01x slower                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.76 ms: 1.01x slower                                                   |
| logging_silent             | 111 ns                                                 | 112 ns: 1.01x slower                                                    |
| sympy_expand               | 484 ms                                                 | 491 ms: 1.01x slower                                                    |
| tomli_loads                | 2.30 sec                                               | 2.34 sec: 1.01x slower                                                  |
| nqueens                    | 87.9 ms                                                | 89.1 ms: 1.01x slower                                                   |
| crypto_pyaes               | 76.7 ms                                                | 78.1 ms: 1.02x slower                                                   |
| regex_compile              | 141 ms                                                 | 144 ms: 1.02x slower                                                    |
| sqlglot_normalize          | 113 ms                                                 | 116 ms: 1.03x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.60 ms: 1.03x slower                                                   |
| richards                   | 49.8 ms                                                | 51.2 ms: 1.03x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                    |
| xml_etree_iterparse        | 108 ms                                                 | 112 ms: 1.03x slower                                                    |
| bench_thread_pool          | 834 us                                                 | 865 us: 1.04x slower                                                    |
| dask                       | 365 ms                                                 | 380 ms: 1.04x slower                                                    |
| genshi_xml                 | 53.4 ms                                                | 55.7 ms: 1.04x slower                                                   |
| pickle_pure_python         | 320 us                                                 | 335 us: 1.05x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 58.1 ms: 1.05x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 68.3 ms: 1.06x slower                                                   |
| meteor_contest             | 109 ms                                                 | 115 ms: 1.06x slower                                                    |
| go                         | 149 ms                                                 | 158 ms: 1.06x slower                                                    |
| pycparser                  | 1.19 sec                                               | 1.26 sec: 1.06x slower                                                  |
| regex_dna                  | 205 ms                                                 | 217 ms: 1.06x slower                                                    |
| json                       | 5.24 ms                                                | 5.57 ms: 1.06x slower                                                   |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                   |
| unpickle_list              | 5.21 us                                                | 5.55 us: 1.06x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                   |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                    |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                                    |
| html5lib                   | 64.8 ms                                                | 69.6 ms: 1.07x slower                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 76.7 ms: 1.08x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.89 sec: 1.08x slower                                                  |
| thrift                     | 784 us                                                 | 856 us: 1.09x slower                                                    |
| nbody                      | 96.0 ms                                                | 105 ms: 1.09x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                   |
| deepcopy                   | 365 us                                                 | 401 us: 1.10x slower                                                    |
| float                      | 78.9 ms                                                | 86.7 ms: 1.10x slower                                                   |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                   |
| fannkuch                   | 405 ms                                                 | 449 ms: 1.11x slower                                                    |
| pprint_pformat             | 1.55 sec                                               | 1.74 sec: 1.12x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.60 us: 1.12x slower                                                   |
| spectral_norm              | 108 ms                                                 | 121 ms: 1.12x slower                                                    |
| deepcopy_memo              | 40.2 us                                                | 45.1 us: 1.12x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.72 ms: 1.14x slower                                                   |
| django_template            | 33.5 ms                                                | 38.2 ms: 1.14x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 853 ms: 1.14x slower                                                    |
| xml_etree_process          | 56.9 ms                                                | 65.1 ms: 1.14x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 93.4 ms: 1.15x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.97 us: 1.15x slower                                                   |
| scimark_sor                | 121 ms                                                 | 141 ms: 1.16x slower                                                    |
| chameleon                  | 6.70 ms                                                | 7.80 ms: 1.16x slower                                                   |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                                   |
| pyflate                    | 434 ms                                                 | 512 ms: 1.18x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.41 us: 1.18x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.16 ms: 1.19x slower                                                   |
| mako                       | 10.7 ms                                                | 12.7 ms: 1.19x slower                                                   |
| scimark_fft                | 345 ms                                                 | 414 ms: 1.20x slower                                                    |
| async_generators           | 374 ms                                                 | 458 ms: 1.23x slower                                                    |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                   |
| flaskblogging              | 7.28 ms                                                | 9.25 ms: 1.27x slower                                                   |
| telco                      | 6.86 ms                                                | 185 ms: 26.94x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (5): xml_etree_parse, tornado_http, json_loads, bench_mp_pool, sqlglot_parse
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.86% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.04x
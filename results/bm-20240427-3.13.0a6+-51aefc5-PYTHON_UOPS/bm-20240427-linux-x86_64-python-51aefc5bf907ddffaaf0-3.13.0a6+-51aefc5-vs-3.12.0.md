# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 314 ms: 1.15x slower                                                   |
| chameleon      | 7.41 ms                                                | 7.49 ms: 1.01x slower                                                  |
| docutils       | 2.77 sec                                               | 3.15 sec: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 348 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 457 ms: 1.26x faster                                                   |
| async_tree_none            | 472 ms                                                 | 376 ms: 1.25x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 959 ms: 1.23x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 967 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 623 ms: 1.16x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 502 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 638 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 90.3 ms: 1.07x slower                                                  |
| pidigits       | 187 ms                                                 | 212 ms: 1.13x slower                                                   |
| nbody          | 97.0 ms                                                | 127 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                  | 1.17x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.89 ms: 1.08x slower                                                  |
| regex_dna      | 212 ms                                                 | 233 ms: 1.10x slower                                                   |
| regex_v8       | 23.1 ms                                                | 26.4 ms: 1.14x slower                                                  |
| regex_compile  | 148 ms                                                 | 178 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| json_loads           | 28.5 us                                                | 27.5 us: 1.04x faster                                                  |
| unpickle             | 15.9 us                                                | 15.5 us: 1.03x faster                                                  |
| pickle_dict          | 35.5 us                                                | 34.9 us: 1.02x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 319 us: 1.02x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| xml_etree_iterparse  | 107 ms                                                 | 112 ms: 1.05x slower                                                   |
| xml_etree_generate   | 89.2 ms                                                | 94.0 ms: 1.05x slower                                                  |
| xml_etree_process    | 61.7 ms                                                | 65.2 ms: 1.06x slower                                                  |
| tomli_loads          | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                 |
| unpickle_pure_python | 230 us                                                 | 289 us: 1.26x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): pickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.14 ms: 1.03x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.5 ms: 1.14x slower                                                  |
| django_template | 34.6 ms                                                | 40.2 ms: 1.16x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.15x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 348 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 457 ms: 1.26x faster                                                   |
| async_tree_none            | 472 ms                                                 | 376 ms: 1.25x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 959 ms: 1.23x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 967 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 623 ms: 1.16x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 502 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 638 ms: 1.14x faster                                                   |
| pathlib                    | 19.3 ms                                                | 18.2 ms: 1.06x faster                                                  |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.5 us: 1.04x faster                                                  |
| unpickle                   | 15.9 us                                                | 15.5 us: 1.03x faster                                                  |
| pickle_dict                | 35.5 us                                                | 34.9 us: 1.02x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 319 us: 1.02x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.33 us: 1.01x faster                                                  |
| generators                 | 31.2 ms                                                | 31.4 ms: 1.01x slower                                                  |
| pickle_list                | 5.08 us                                                | 5.12 us: 1.01x slower                                                  |
| chameleon                  | 7.41 ms                                                | 7.49 ms: 1.01x slower                                                  |
| deepcopy                   | 371 us                                                 | 380 us: 1.02x slower                                                   |
| async_generators           | 463 ms                                                 | 475 ms: 1.03x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| python_startup_no_site     | 6.94 ms                                                | 7.14 ms: 1.03x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                   |
| raytrace                   | 312 ms                                                 | 324 ms: 1.04x slower                                                   |
| coroutines                 | 23.2 ms                                                | 24.0 ms: 1.04x slower                                                  |
| sympy_sum                  | 169 ms                                                 | 176 ms: 1.04x slower                                                   |
| dask                       | 372 ms                                                 | 387 ms: 1.04x slower                                                   |
| xml_etree_iterparse        | 107 ms                                                 | 112 ms: 1.05x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                 |
| logging_format             | 7.23 us                                                | 7.62 us: 1.05x slower                                                  |
| xml_etree_generate         | 89.2 ms                                                | 94.0 ms: 1.05x slower                                                  |
| logging_simple             | 6.46 us                                                | 6.81 us: 1.05x slower                                                  |
| deepcopy_memo              | 40.7 us                                                | 43.0 us: 1.06x slower                                                  |
| xml_etree_process          | 61.7 ms                                                | 65.2 ms: 1.06x slower                                                  |
| float                      | 84.7 ms                                                | 90.3 ms: 1.07x slower                                                  |
| gc_traversal               | 3.79 ms                                                | 4.06 ms: 1.07x slower                                                  |
| bench_thread_pool          | 842 us                                                 | 902 us: 1.07x slower                                                   |
| sqlite_synth               | 2.83 us                                                | 3.04 us: 1.07x slower                                                  |
| sympy_str                  | 300 ms                                                 | 322 ms: 1.07x slower                                                   |
| mdp                        | 2.63 sec                                               | 2.83 sec: 1.07x slower                                                 |
| sqlglot_transpile          | 1.68 ms                                                | 1.81 ms: 1.08x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.89 ms: 1.08x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.34 ms: 1.08x slower                                                  |
| asyncio_tcp                | 491 ms                                                 | 530 ms: 1.08x slower                                                   |
| aiohttp                    | 1.15 ms                                                | 1.24 ms: 1.08x slower                                                  |
| tomli_loads                | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                 |
| sympy_integrate            | 21.4 ms                                                | 23.3 ms: 1.09x slower                                                  |
| meteor_contest             | 112 ms                                                 | 123 ms: 1.09x slower                                                   |
| dulwich_log                | 68.5 ms                                                | 75.0 ms: 1.09x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.49 ms: 1.10x slower                                                  |
| regex_dna                  | 212 ms                                                 | 233 ms: 1.10x slower                                                   |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| sympy_expand               | 478 ms                                                 | 537 ms: 1.12x slower                                                   |
| crypto_pyaes               | 81.9 ms                                                | 92.3 ms: 1.13x slower                                                  |
| pycparser                  | 1.18 sec                                               | 1.34 sec: 1.13x slower                                                 |
| pidigits                   | 187 ms                                                 | 212 ms: 1.13x slower                                                   |
| mako                       | 11.9 ms                                                | 13.5 ms: 1.14x slower                                                  |
| docutils                   | 2.77 sec                                               | 3.15 sec: 1.14x slower                                                 |
| regex_v8                   | 23.1 ms                                                | 26.4 ms: 1.14x slower                                                  |
| comprehensions             | 21.8 us                                                | 24.9 us: 1.14x slower                                                  |
| 2to3                       | 274 ms                                                 | 314 ms: 1.15x slower                                                   |
| sqlglot_normalize          | 110 ms                                                 | 128 ms: 1.16x slower                                                   |
| django_template            | 34.6 ms                                                | 40.2 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.94 ms: 1.17x slower                                                  |
| sqlglot_optimize           | 54.8 ms                                                | 64.5 ms: 1.18x slower                                                  |
| scimark_fft                | 382 ms                                                 | 452 ms: 1.18x slower                                                   |
| chaos                      | 67.0 ms                                                | 79.3 ms: 1.18x slower                                                  |
| deltablue                  | 3.72 ms                                                | 4.40 ms: 1.19x slower                                                  |
| fannkuch                   | 417 ms                                                 | 497 ms: 1.19x slower                                                   |
| regex_compile              | 148 ms                                                 | 178 ms: 1.20x slower                                                   |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 90.6 ms: 1.21x slower                                                  |
| richards                   | 45.8 ms                                                | 55.5 ms: 1.21x slower                                                  |
| richards_super             | 51.5 ms                                                | 62.4 ms: 1.21x slower                                                  |
| scimark_sor                | 129 ms                                                 | 157 ms: 1.22x slower                                                   |
| pprint_safe_repr           | 776 ms                                                 | 956 ms: 1.23x slower                                                   |
| spectral_norm              | 115 ms                                                 | 143 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 158 us                                                 | 197 us: 1.25x slower                                                   |
| pyflate                    | 482 ms                                                 | 606 ms: 1.26x slower                                                   |
| unpickle_pure_python       | 230 us                                                 | 289 us: 1.26x slower                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.99 sec: 1.27x slower                                                 |
| coverage                   | 72.7 ms                                                | 92.7 ms: 1.27x slower                                                  |
| telco                      | 7.10 ms                                                | 9.18 ms: 1.29x slower                                                  |
| nbody                      | 97.0 ms                                                | 127 ms: 1.31x slower                                                   |
| nqueens                    | 83.3 ms                                                | 110 ms: 1.32x slower                                                   |
| go                         | 139 ms                                                 | 197 ms: 1.41x slower                                                   |
| scimark_lu                 | 118 ms                                                 | 172 ms: 1.46x slower                                                   |
| hexiom                     | 6.41 ms                                                | 9.97 ms: 1.55x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (7): mypy2, tornado_http, json, bench_mp_pool, logging_silent, pickle, unpickle_list
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.97x
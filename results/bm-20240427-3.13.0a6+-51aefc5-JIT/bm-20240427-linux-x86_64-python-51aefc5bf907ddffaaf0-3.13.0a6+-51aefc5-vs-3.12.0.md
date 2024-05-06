# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.02x faster
- HPT reliability: 89.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 282 ms: 1.03x slower                                                   |
| chameleon      | 7.41 ms                                                | 7.03 ms: 1.05x faster                                                  |
| docutils       | 2.77 sec                                               | 2.96 sec: 1.07x slower                                                 |
| tornado_http   | 103 ms                                                 | 96.6 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                   |
| async_tree_none            | 472 ms                                                 | 361 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 946 ms: 1.25x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 467 ms: 1.24x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 947 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 607 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 76.9 ms: 1.10x faster                                                  |
| nbody          | 97.0 ms                                                | 92.8 ms: 1.04x faster                                                  |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 143 ms: 1.04x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.64 ms: 1.01x slower                                                  |
| regex_dna      | 212 ms                                                 | 218 ms: 1.03x slower                                                   |
| regex_v8       | 23.1 ms                                                | 24.3 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.04 sec: 1.14x faster                                                 |
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| pickle_pure_python   | 324 us                                                 | 311 us: 1.04x faster                                                   |
| json_loads           | 28.5 us                                                | 27.3 us: 1.04x faster                                                  |
| unpickle             | 15.9 us                                                | 15.2 us: 1.04x faster                                                  |
| xml_etree_iterparse  | 107 ms                                                 | 104 ms: 1.03x faster                                                   |
| pickle_dict          | 35.5 us                                                | 34.7 us: 1.02x faster                                                  |
| xml_etree_process    | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 87.9 ms: 1.01x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.11 us: 1.00x slower                                                  |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| unpickle_list        | 5.29 us                                                | 5.36 us: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                  |
| unpickle_pure_python | 230 us                                                 | 235 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.61 ms: 1.10x slower                                                  |
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.7 ms: 1.12x faster                                                  |
| django_template | 34.6 ms                                                | 37.0 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                   |
| async_tree_none            | 472 ms                                                 | 361 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 946 ms: 1.25x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 467 ms: 1.24x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 947 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 607 ms: 1.19x faster                                                   |
| comprehensions             | 21.8 us                                                | 18.3 us: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                   |
| tomli_loads                | 2.33 sec                                               | 2.04 sec: 1.14x faster                                                 |
| raytrace                   | 312 ms                                                 | 279 ms: 1.12x faster                                                   |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.12x faster                                                  |
| scimark_fft                | 382 ms                                                 | 344 ms: 1.11x faster                                                   |
| crypto_pyaes               | 81.9 ms                                                | 74.3 ms: 1.10x faster                                                  |
| float                      | 84.7 ms                                                | 76.9 ms: 1.10x faster                                                  |
| pathlib                    | 19.3 ms                                                | 17.7 ms: 1.09x faster                                                  |
| logging_format             | 7.23 us                                                | 6.63 us: 1.09x faster                                                  |
| fannkuch                   | 417 ms                                                 | 383 ms: 1.09x faster                                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 69.2 ms: 1.09x faster                                                  |
| logging_simple             | 6.46 us                                                | 5.97 us: 1.08x faster                                                  |
| tornado_http               | 103 ms                                                 | 96.6 ms: 1.06x faster                                                  |
| richards                   | 45.8 ms                                                | 43.2 ms: 1.06x faster                                                  |
| chameleon                  | 7.41 ms                                                | 7.03 ms: 1.05x faster                                                  |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| chaos                      | 67.0 ms                                                | 63.7 ms: 1.05x faster                                                  |
| richards_super             | 51.5 ms                                                | 49.0 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 776 ms                                                 | 740 ms: 1.05x faster                                                   |
| nbody                      | 97.0 ms                                                | 92.8 ms: 1.04x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 311 us: 1.04x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.3 us: 1.04x faster                                                  |
| pyflate                    | 482 ms                                                 | 463 ms: 1.04x faster                                                   |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.04x faster                                                  |
| regex_compile              | 148 ms                                                 | 143 ms: 1.04x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 39.3 us: 1.04x faster                                                  |
| json                       | 5.26 ms                                                | 5.10 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.25 us: 1.03x faster                                                  |
| generators                 | 31.2 ms                                                | 30.4 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.57 sec                                               | 1.53 sec: 1.03x faster                                                 |
| xml_etree_iterparse        | 107 ms                                                 | 104 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.94 ms: 1.02x faster                                                  |
| pickle_dict                | 35.5 us                                                | 34.7 us: 1.02x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.02x faster                                                  |
| xml_etree_process          | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                  |
| logging_silent             | 104 ns                                                 | 103 ns: 1.02x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 87.9 ms: 1.01x faster                                                  |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.66 ms: 1.01x faster                                                  |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                   |
| mdp                        | 2.63 sec                                               | 2.62 sec: 1.01x faster                                                 |
| deepcopy                   | 371 us                                                 | 369 us: 1.01x faster                                                   |
| async_generators           | 463 ms                                                 | 465 ms: 1.00x slower                                                   |
| pickle_list                | 5.08 us                                                | 5.11 us: 1.00x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| sympy_sum                  | 169 ms                                                 | 170 ms: 1.01x slower                                                   |
| regex_effbot               | 3.61 ms                                                | 3.64 ms: 1.01x slower                                                  |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                   |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| dask                       | 372 ms                                                 | 376 ms: 1.01x slower                                                   |
| unpickle_list              | 5.29 us                                                | 5.36 us: 1.01x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                  |
| dulwich_log                | 68.5 ms                                                | 69.6 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 230 us                                                 | 235 us: 1.02x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                   |
| 2to3                       | 274 ms                                                 | 282 ms: 1.03x slower                                                   |
| regex_dna                  | 212 ms                                                 | 218 ms: 1.03x slower                                                   |
| bench_thread_pool          | 842 us                                                 | 870 us: 1.03x slower                                                   |
| deltablue                  | 3.72 ms                                                | 3.85 ms: 1.04x slower                                                  |
| sqlglot_normalize          | 110 ms                                                 | 115 ms: 1.04x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                 |
| sympy_expand               | 478 ms                                                 | 502 ms: 1.05x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 24.3 ms: 1.05x slower                                                  |
| sympy_integrate            | 21.4 ms                                                | 22.6 ms: 1.05x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.06x slower                                                  |
| gc_traversal               | 3.79 ms                                                | 4.02 ms: 1.06x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                  |
| sqlglot_optimize           | 54.8 ms                                                | 58.3 ms: 1.06x slower                                                  |
| asyncio_tcp                | 491 ms                                                 | 522 ms: 1.06x slower                                                   |
| docutils                   | 2.77 sec                                               | 2.96 sec: 1.07x slower                                                 |
| django_template            | 34.6 ms                                                | 37.0 ms: 1.07x slower                                                  |
| scimark_sor                | 129 ms                                                 | 140 ms: 1.08x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.61 ms: 1.10x slower                                                  |
| typing_runtime_protocols   | 158 us                                                 | 175 us: 1.11x slower                                                   |
| nqueens                    | 83.3 ms                                                | 92.1 ms: 1.11x slower                                                  |
| hexiom                     | 6.41 ms                                                | 7.16 ms: 1.12x slower                                                  |
| go                         | 139 ms                                                 | 156 ms: 1.12x slower                                                   |
| scimark_lu                 | 118 ms                                                 | 136 ms: 1.15x slower                                                   |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.21x slower                                                  |
| telco                      | 7.10 ms                                                | 8.66 ms: 1.22x slower                                                  |
| coverage                   | 72.7 ms                                                | 92.2 ms: 1.27x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (5): mypy2, pycparser, spectral_norm, sympy_str, bench_mp_pool
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 89.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
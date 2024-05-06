# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.04x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 271 ms: 1.01x faster                                                   |
| chameleon      | 7.41 ms                                                | 7.29 ms: 1.02x faster                                                  |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                 |
| tornado_http   | 103 ms                                                 | 94.4 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                   |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 908 ms: 1.27x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.9 ms: 1.07x faster                                                  |
| nbody          | 97.0 ms                                                | 92.5 ms: 1.05x faster                                                  |
| pidigits       | 187 ms                                                 | 194 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 136 ms: 1.09x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.67 ms: 1.02x slower                                                  |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                   |
| regex_v8       | 23.1 ms                                                | 24.9 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 306 us: 1.06x faster                                                   |
| tomli_loads          | 2.33 sec                                               | 2.20 sec: 1.06x faster                                                 |
| unpickle_pure_python | 230 us                                                 | 219 us: 1.05x faster                                                   |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                  |
| unpickle             | 15.9 us                                                | 15.3 us: 1.03x faster                                                  |
| xml_etree_process    | 61.7 ms                                                | 60.7 ms: 1.02x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 87.8 ms: 1.02x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| unpickle_list        | 5.29 us                                                | 5.32 us: 1.01x slower                                                  |
| pickle_dict          | 35.5 us                                                | 35.8 us: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.11 ms: 1.03x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                  |
| django_template | 34.6 ms                                                | 34.9 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                   |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                   |
| comprehensions             | 21.8 us                                                | 16.8 us: 1.30x faster                                                  |
| async_tree_io              | 1.16 sec                                               | 908 ms: 1.27x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                   |
| raytrace                   | 312 ms                                                 | 263 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                   |
| deltablue                  | 3.72 ms                                                | 3.23 ms: 1.15x faster                                                  |
| logging_format             | 7.23 us                                                | 6.41 us: 1.13x faster                                                  |
| mypy2                      | 830 ms                                                 | 737 ms: 1.13x faster                                                   |
| logging_simple             | 6.46 us                                                | 5.77 us: 1.12x faster                                                  |
| chaos                      | 67.0 ms                                                | 60.5 ms: 1.11x faster                                                  |
| pathlib                    | 19.3 ms                                                | 17.7 ms: 1.09x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 74.8 ms: 1.09x faster                                                  |
| regex_compile              | 148 ms                                                 | 136 ms: 1.09x faster                                                   |
| tornado_http               | 103 ms                                                 | 94.4 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 69.3 ms: 1.08x faster                                                  |
| mako                       | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                   |
| float                      | 84.7 ms                                                | 78.9 ms: 1.07x faster                                                  |
| sympy_str                  | 300 ms                                                 | 280 ms: 1.07x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.06x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 306 us: 1.06x faster                                                   |
| tomli_loads                | 2.33 sec                                               | 2.20 sec: 1.06x faster                                                 |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                  |
| generators                 | 31.2 ms                                                | 29.6 ms: 1.06x faster                                                  |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 230 us                                                 | 219 us: 1.05x faster                                                   |
| nbody                      | 97.0 ms                                                | 92.5 ms: 1.05x faster                                                  |
| async_generators           | 463 ms                                                 | 444 ms: 1.04x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 39.1 us: 1.04x faster                                                  |
| dulwich_log                | 68.5 ms                                                | 65.8 ms: 1.04x faster                                                  |
| fannkuch                   | 417 ms                                                 | 401 ms: 1.04x faster                                                   |
| scimark_fft                | 382 ms                                                 | 369 ms: 1.04x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                  |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.03x faster                                                  |
| nqueens                    | 83.3 ms                                                | 80.6 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.24 us: 1.03x faster                                                  |
| scimark_sor                | 129 ms                                                 | 126 ms: 1.03x faster                                                   |
| deepcopy                   | 371 us                                                 | 361 us: 1.03x faster                                                   |
| logging_silent             | 104 ns                                                 | 102 ns: 1.02x faster                                                   |
| pprint_safe_repr           | 776 ms                                                 | 759 ms: 1.02x faster                                                   |
| json                       | 5.26 ms                                                | 5.16 ms: 1.02x faster                                                  |
| chameleon                  | 7.41 ms                                                | 7.29 ms: 1.02x faster                                                  |
| xml_etree_process          | 61.7 ms                                                | 60.7 ms: 1.02x faster                                                  |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                                 |
| xml_etree_generate         | 89.2 ms                                                | 87.8 ms: 1.02x faster                                                  |
| sympy_expand               | 478 ms                                                 | 472 ms: 1.01x faster                                                   |
| pickle_list                | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| 2to3                       | 274 ms                                                 | 271 ms: 1.01x faster                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.55 sec: 1.01x faster                                                 |
| bench_thread_pool          | 842 us                                                 | 835 us: 1.01x faster                                                   |
| spectral_norm              | 115 ms                                                 | 114 ms: 1.01x faster                                                   |
| gc_traversal               | 3.79 ms                                                | 3.77 ms: 1.01x faster                                                  |
| hexiom                     | 6.41 ms                                                | 6.37 ms: 1.01x faster                                                  |
| meteor_contest             | 112 ms                                                 | 112 ms: 1.01x faster                                                   |
| mdp                        | 2.63 sec                                               | 2.62 sec: 1.01x faster                                                 |
| pyflate                    | 482 ms                                                 | 484 ms: 1.00x slower                                                   |
| unpickle_list              | 5.29 us                                                | 5.32 us: 1.01x slower                                                  |
| pickle_dict                | 35.5 us                                                | 35.8 us: 1.01x slower                                                  |
| sqlglot_optimize           | 54.8 ms                                                | 55.3 ms: 1.01x slower                                                  |
| django_template            | 34.6 ms                                                | 34.9 ms: 1.01x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.01x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.67 ms: 1.02x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.26 ms: 1.02x slower                                                  |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                 |
| go                         | 139 ms                                                 | 143 ms: 1.02x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.11 ms: 1.03x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.20 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 2.92 us: 1.03x slower                                                  |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                 |
| pidigits                   | 187 ms                                                 | 194 ms: 1.03x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 509 ms: 1.04x slower                                                   |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                                  |
| richards                   | 45.8 ms                                                | 48.0 ms: 1.05x slower                                                  |
| richards_super             | 51.5 ms                                                | 54.3 ms: 1.05x slower                                                  |
| typing_runtime_protocols   | 158 us                                                 | 167 us: 1.06x slower                                                   |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 24.9 ms: 1.08x slower                                                  |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                  |
| telco                      | 7.10 ms                                                | 8.68 ms: 1.22x slower                                                  |
| coverage                   | 72.7 ms                                                | 92.7 ms: 1.28x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (7): dask, coroutines, bench_mp_pool, sqlglot_normalize, scimark_lu, xml_etree_iterparse, xml_etree_parse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x
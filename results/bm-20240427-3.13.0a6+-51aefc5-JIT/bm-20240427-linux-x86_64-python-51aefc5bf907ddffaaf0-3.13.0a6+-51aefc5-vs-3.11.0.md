# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.04x faster
- HPT reliability: 69.49%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 282 ms: 1.07x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                  |
| docutils       | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                 |
| html5lib       | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                  |
| tornado_http   | 98.1 ms                                                | 96.6 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 361 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 946 ms: 1.37x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.8 ms: 1.03x faster                                                  |
| float          | 78.9 ms                                                | 76.9 ms: 1.03x faster                                                  |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 143 ms: 1.01x slower                                                   |
| regex_effbot   | 3.51 ms                                                | 3.64 ms: 1.04x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.3 ms: 1.06x slower                                                  |
| regex_dna      | 205 ms                                                 | 218 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.04 sec: 1.13x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| json_loads           | 29.2 us                                                | 27.3 us: 1.07x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 235 us: 1.03x faster                                                   |
| pickle_pure_python   | 320 us                                                 | 311 us: 1.03x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.7 us: 1.00x slower                                                  |
| unpickle_list        | 5.21 us                                                | 5.36 us: 1.03x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                  |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 87.9 ms: 1.08x slower                                                  |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.11 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.61 ms: 1.27x slower                                                  |
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 57.9 ms: 1.08x slower                                                  |
| django_template | 33.5 ms                                                | 37.0 ms: 1.10x slower                                                  |
| genshi_text     | 22.5 ms                                                | 26.5 ms: 1.18x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 175 us: 2.98x faster                                                   |
| generators                 | 74.9 ms                                                | 30.4 ms: 2.46x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 522 ms: 1.68x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                 |
| async_tree_none            | 528 ms                                                 | 361 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| pylint                     | 476 ms                                                 | 346 ms: 1.38x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 946 ms: 1.37x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                   |
| comprehensions             | 23.6 us                                                | 18.3 us: 1.29x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| richards_super             | 61.9 ms                                                | 49.0 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                   |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.18x faster                                                  |
| richards                   | 49.8 ms                                                | 43.2 ms: 1.15x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.04 sec: 1.13x faster                                                 |
| chaos                      | 71.9 ms                                                | 63.7 ms: 1.13x faster                                                  |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.07x faster                                                  |
| json_loads                 | 29.2 us                                                | 27.3 us: 1.07x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.62 sec: 1.06x faster                                                 |
| fannkuch                   | 405 ms                                                 | 383 ms: 1.06x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.05x faster                                                  |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.05x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.97 us: 1.04x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| nbody                      | 96.0 ms                                                | 92.8 ms: 1.03x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 74.3 ms: 1.03x faster                                                  |
| djangocms                  | 33.5 us                                                | 32.5 us: 1.03x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 235 us: 1.03x faster                                                   |
| pickle_pure_python         | 320 us                                                 | 311 us: 1.03x faster                                                   |
| json                       | 5.24 ms                                                | 5.10 ms: 1.03x faster                                                  |
| logging_format             | 6.81 us                                                | 6.63 us: 1.03x faster                                                  |
| float                      | 78.9 ms                                                | 76.9 ms: 1.03x faster                                                  |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 69.2 ms: 1.02x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.85 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.94 ms: 1.02x faster                                                  |
| tornado_http               | 98.1 ms                                                | 96.6 ms: 1.01x faster                                                  |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                                 |
| pprint_safe_repr           | 747 ms                                                 | 740 ms: 1.01x faster                                                   |
| scimark_fft                | 345 ms                                                 | 344 ms: 1.00x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 4.02 ms: 1.00x slower                                                  |
| pickle_dict                | 34.6 us                                                | 34.7 us: 1.00x slower                                                  |
| sympy_sum                  | 169 ms                                                 | 170 ms: 1.01x slower                                                   |
| regex_compile              | 141 ms                                                 | 143 ms: 1.01x slower                                                   |
| deepcopy                   | 365 us                                                 | 369 us: 1.01x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.25 us: 1.01x slower                                                  |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                                   |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                   |
| unpickle_list              | 5.21 us                                                | 5.36 us: 1.03x slower                                                  |
| dask                       | 365 ms                                                 | 376 ms: 1.03x slower                                                   |
| sympy_expand               | 484 ms                                                 | 502 ms: 1.04x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.64 ms: 1.04x slower                                                  |
| hexiom                     | 6.89 ms                                                | 7.16 ms: 1.04x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 870 us: 1.04x slower                                                   |
| thrift                     | 784 us                                                 | 821 us: 1.05x slower                                                   |
| nqueens                    | 87.9 ms                                                | 92.1 ms: 1.05x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                  |
| go                         | 149 ms                                                 | 156 ms: 1.05x slower                                                   |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 58.3 ms: 1.05x slower                                                  |
| html5lib                   | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                  |
| spectral_norm              | 108 ms                                                 | 114 ms: 1.06x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 24.3 ms: 1.06x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                  |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.07x slower                                                   |
| 2to3                       | 264 ms                                                 | 282 ms: 1.07x slower                                                   |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                  |
| pyflate                    | 434 ms                                                 | 463 ms: 1.07x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 69.6 ms: 1.08x slower                                                  |
| genshi_xml                 | 53.4 ms                                                | 57.9 ms: 1.08x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 87.9 ms: 1.08x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.10x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                  |
| django_template            | 33.5 ms                                                | 37.0 ms: 1.10x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.11 us: 1.11x slower                                                  |
| scimark_sor                | 121 ms                                                 | 140 ms: 1.15x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 136 ms: 1.17x slower                                                   |
| coverage                   | 78.8 ms                                                | 92.2 ms: 1.17x slower                                                  |
| genshi_text                | 22.5 ms                                                | 26.5 ms: 1.18x slower                                                  |
| mypy2                      | 686 ms                                                 | 813 ms: 1.19x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                  |
| async_generators           | 374 ms                                                 | 465 ms: 1.24x slower                                                   |
| telco                      | 6.86 ms                                                | 8.66 ms: 1.26x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.61 ms: 1.27x slower                                                  |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (3): mako, bench_mp_pool, sympy_str
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 69.49% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x
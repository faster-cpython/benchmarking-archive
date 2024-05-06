# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.06x faster
- HPT reliability: 96.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.02x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.29 ms: 1.09x slower                                                  |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                 |
| html5lib       | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                  |
| tornado_http   | 98.1 ms                                                | 94.4 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 908 ms: 1.42x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.5 ms: 1.04x faster                                                  |
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                   |
| regex_effbot   | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.9 ms: 1.09x slower                                                  |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 219 us: 1.10x faster                                                   |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.20 sec: 1.05x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.05x faster                                                   |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.32 us: 1.02x slower                                                  |
| pickle_dict          | 34.6 us                                                | 35.8 us: 1.04x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 60.7 ms: 1.07x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 87.8 ms: 1.08x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.02 us: 1.09x slower                                                  |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| unpickle             | 13.8 us                                                | 15.3 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 54.0 ms: 1.01x slower                                                  |
| mako            | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                  |
| django_template | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                  |
| genshi_text     | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 167 us: 3.11x faster                                                   |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 509 ms: 1.72x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                 |
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                   |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 908 ms: 1.42x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.21x faster                                                  |
| chaos                      | 71.9 ms                                                | 60.5 ms: 1.19x faster                                                  |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.17x faster                                                  |
| raytrace                   | 309 ms                                                 | 263 ms: 1.17x faster                                                   |
| richards_super             | 61.9 ms                                                | 54.3 ms: 1.14x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.28 ms: 1.12x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 219 us: 1.10x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                  |
| nqueens                    | 87.9 ms                                                | 80.6 ms: 1.09x faster                                                  |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.37 ms: 1.08x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.77 ms: 1.06x faster                                                  |
| logging_format             | 6.81 us                                                | 6.41 us: 1.06x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.62 sec: 1.06x faster                                                 |
| sympy_str                  | 297 ms                                                 | 280 ms: 1.06x faster                                                   |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                                  |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                  |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.05x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.20 sec: 1.05x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.05x faster                                                   |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                   |
| tornado_http               | 98.1 ms                                                | 94.4 ms: 1.04x faster                                                  |
| richards                   | 49.8 ms                                                | 48.0 ms: 1.04x faster                                                  |
| nbody                      | 96.0 ms                                                | 92.5 ms: 1.04x faster                                                  |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                   |
| sympy_expand               | 484 ms                                                 | 472 ms: 1.03x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 39.1 us: 1.03x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 74.8 ms: 1.03x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                   |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 69.3 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                   |
| json                       | 5.24 ms                                                | 5.16 ms: 1.02x faster                                                  |
| deepcopy                   | 365 us                                                 | 361 us: 1.01x faster                                                   |
| fannkuch                   | 405 ms                                                 | 401 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.55 sec: 1.00x faster                                                 |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.24 us: 1.01x slower                                                  |
| genshi_xml                 | 53.4 ms                                                | 54.0 ms: 1.01x slower                                                  |
| dask                       | 365 ms                                                 | 370 ms: 1.01x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 759 ms: 1.02x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 118 ms: 1.02x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 65.8 ms: 1.02x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.32 us: 1.02x slower                                                  |
| 2to3                       | 264 ms                                                 | 271 ms: 1.02x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                   |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.02x slower                                                   |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                  |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.20 ms: 1.03x slower                                                  |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.04x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.8 us: 1.04x slower                                                  |
| django_template            | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.04x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                  |
| spectral_norm              | 108 ms                                                 | 114 ms: 1.05x slower                                                   |
| html5lib                   | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 60.7 ms: 1.07x slower                                                  |
| scimark_fft                | 345 ms                                                 | 369 ms: 1.07x slower                                                   |
| mypy2                      | 686 ms                                                 | 737 ms: 1.07x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 87.8 ms: 1.08x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.29 ms: 1.09x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 24.9 ms: 1.09x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.02 us: 1.09x slower                                                  |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.11x slower                                                  |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                   |
| pyflate                    | 434 ms                                                 | 484 ms: 1.12x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.92 us: 1.14x slower                                                  |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                  |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.22x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| telco                      | 6.86 ms                                                | 8.68 ms: 1.27x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (3): float, bench_thread_pool, sqlglot_optimize
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
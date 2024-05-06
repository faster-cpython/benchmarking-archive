# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 314 ms: 1.19x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.49 ms: 1.12x slower                                                  |
| docutils       | 2.66 sec                                               | 3.15 sec: 1.18x slower                                                 |
| html5lib       | 64.8 ms                                                | 71.8 ms: 1.11x slower                                                  |
| tornado_http   | 98.1 ms                                                | 102 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 348 ms: 1.41x faster                                                   |
| async_tree_none            | 528 ms                                                 | 376 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 959 ms: 1.35x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 967 ms: 1.33x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 502 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 623 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 212 ms: 1.09x slower                                                   |
| float          | 78.9 ms                                                | 90.3 ms: 1.14x slower                                                  |
| nbody          | 96.0 ms                                                | 127 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.89 ms: 1.11x slower                                                  |
| regex_dna      | 205 ms                                                 | 233 ms: 1.14x slower                                                   |
| regex_v8       | 22.9 ms                                                | 26.4 ms: 1.15x slower                                                  |
| regex_compile  | 141 ms                                                 | 178 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 319 us: 1.00x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.9 us: 1.01x slower                                                  |
| unpickle_list        | 5.21 us                                                | 5.29 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 112 ms: 1.03x slower                                                   |
| pickle               | 11.0 us                                                | 11.6 us: 1.05x slower                                                  |
| tomli_loads          | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.12 us: 1.12x slower                                                  |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 65.2 ms: 1.15x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 94.0 ms: 1.16x slower                                                  |
| unpickle_pure_python | 242 us                                                 | 289 us: 1.20x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.14 ms: 1.19x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 33.5 ms                                                | 40.2 ms: 1.20x slower                                                  |
| mako            | 10.7 ms                                                | 13.5 ms: 1.27x slower                                                  |
| genshi_xml      | 53.4 ms                                                | 69.1 ms: 1.29x slower                                                  |
| genshi_text     | 22.5 ms                                                | 30.8 ms: 1.37x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 197 us: 2.63x faster                                                   |
| generators                 | 74.9 ms                                                | 31.4 ms: 2.38x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 530 ms: 1.65x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 348 ms: 1.41x faster                                                   |
| async_tree_none            | 528 ms                                                 | 376 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                   |
| pylint                     | 476 ms                                                 | 350 ms: 1.36x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 959 ms: 1.35x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 967 ms: 1.33x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 502 ms: 1.27x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 623 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                   |
| coroutines                 | 27.0 ms                                                | 24.0 ms: 1.12x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| logging_silent             | 111 ns                                                 | 104 ns: 1.06x faster                                                   |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                                  |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                                  |
| pathlib                    | 18.5 ms                                                | 18.2 ms: 1.02x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 319 us: 1.00x faster                                                   |
| richards_super             | 61.9 ms                                                | 62.4 ms: 1.01x slower                                                  |
| pickle_dict                | 34.6 us                                                | 34.9 us: 1.01x slower                                                  |
| gc_traversal               | 4.01 ms                                                | 4.06 ms: 1.01x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.29 us: 1.01x slower                                                  |
| mdp                        | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 112 ms: 1.03x slower                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.81 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.33 us: 1.04x slower                                                  |
| deepcopy                   | 365 us                                                 | 380 us: 1.04x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 176 ms: 1.04x slower                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.49 ms: 1.04x slower                                                  |
| tornado_http               | 98.1 ms                                                | 102 ms: 1.04x slower                                                   |
| raytrace                   | 309 ms                                                 | 324 ms: 1.05x slower                                                   |
| pickle                     | 11.0 us                                                | 11.6 us: 1.05x slower                                                  |
| comprehensions             | 23.6 us                                                | 24.9 us: 1.05x slower                                                  |
| dask                       | 365 ms                                                 | 387 ms: 1.06x slower                                                   |
| deepcopy_memo              | 40.2 us                                                | 43.0 us: 1.07x slower                                                  |
| thrift                     | 784 us                                                 | 844 us: 1.08x slower                                                   |
| bench_thread_pool          | 834 us                                                 | 902 us: 1.08x slower                                                   |
| sympy_str                  | 297 ms                                                 | 322 ms: 1.08x slower                                                   |
| sympy_integrate            | 21.5 ms                                                | 23.3 ms: 1.09x slower                                                  |
| pidigits                   | 194 ms                                                 | 212 ms: 1.09x slower                                                   |
| logging_simple             | 6.22 us                                                | 6.81 us: 1.10x slower                                                  |
| tomli_loads                | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                 |
| chaos                      | 71.9 ms                                                | 79.3 ms: 1.10x slower                                                  |
| html5lib                   | 64.8 ms                                                | 71.8 ms: 1.11x slower                                                  |
| sympy_expand               | 484 ms                                                 | 537 ms: 1.11x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.89 ms: 1.11x slower                                                  |
| richards                   | 49.8 ms                                                | 55.5 ms: 1.11x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.12 us: 1.12x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.34 ms: 1.12x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.24 ms: 1.12x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.49 ms: 1.12x slower                                                  |
| logging_format             | 6.81 us                                                | 7.62 us: 1.12x slower                                                  |
| deltablue                  | 3.92 ms                                                | 4.40 ms: 1.12x slower                                                  |
| pycparser                  | 1.19 sec                                               | 1.34 sec: 1.13x slower                                                 |
| meteor_contest             | 109 ms                                                 | 123 ms: 1.13x slower                                                   |
| sqlglot_normalize          | 113 ms                                                 | 128 ms: 1.13x slower                                                   |
| regex_dna                  | 205 ms                                                 | 233 ms: 1.14x slower                                                   |
| float                      | 78.9 ms                                                | 90.3 ms: 1.14x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 65.2 ms: 1.15x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 26.4 ms: 1.15x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 94.0 ms: 1.16x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 75.0 ms: 1.16x slower                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 64.5 ms: 1.17x slower                                                  |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.94 ms: 1.18x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 3.04 us: 1.18x slower                                                  |
| docutils                   | 2.66 sec                                               | 3.15 sec: 1.18x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.14 ms: 1.19x slower                                                  |
| 2to3                       | 264 ms                                                 | 314 ms: 1.19x slower                                                   |
| unpickle_pure_python       | 242 us                                                 | 289 us: 1.20x slower                                                   |
| django_template            | 33.5 ms                                                | 40.2 ms: 1.20x slower                                                  |
| mypy2                      | 686 ms                                                 | 823 ms: 1.20x slower                                                   |
| crypto_pyaes               | 76.7 ms                                                | 92.3 ms: 1.20x slower                                                  |
| fannkuch                   | 405 ms                                                 | 497 ms: 1.23x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                  |
| nqueens                    | 87.9 ms                                                | 110 ms: 1.25x slower                                                   |
| regex_compile              | 141 ms                                                 | 178 ms: 1.26x slower                                                   |
| mako                       | 10.7 ms                                                | 13.5 ms: 1.27x slower                                                  |
| async_generators           | 374 ms                                                 | 475 ms: 1.27x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 956 ms: 1.28x slower                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 90.6 ms: 1.28x slower                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.99 sec: 1.28x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 69.1 ms: 1.29x slower                                                  |
| scimark_sor                | 121 ms                                                 | 157 ms: 1.29x slower                                                   |
| scimark_fft                | 345 ms                                                 | 452 ms: 1.31x slower                                                   |
| nbody                      | 96.0 ms                                                | 127 ms: 1.32x slower                                                   |
| spectral_norm              | 108 ms                                                 | 143 ms: 1.32x slower                                                   |
| go                         | 149 ms                                                 | 197 ms: 1.33x slower                                                   |
| telco                      | 6.86 ms                                                | 9.18 ms: 1.34x slower                                                  |
| genshi_text                | 22.5 ms                                                | 30.8 ms: 1.37x slower                                                  |
| pyflate                    | 434 ms                                                 | 606 ms: 1.40x slower                                                   |
| hexiom                     | 6.89 ms                                                | 9.97 ms: 1.45x slower                                                  |
| scimark_lu                 | 116 ms                                                 | 172 ms: 1.48x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (2): bench_mp_pool, json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.04x
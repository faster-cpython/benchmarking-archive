# Results vs. 3.11.0

- fork: gaogaotiantian
- ref: optimize_sys_settrac
- machine: linux-x86_64
- commit hash: a65be06
- commit date: 2024-03-27
- overall geometric mean: 1.03x faster
- HPT reliability: 62.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                           |
| chameleon      | 6.70 ms                                                | 7.00 ms: 1.05x slower                                                          |
| docutils       | 2.66 sec                                               | 2.89 sec: 1.09x slower                                                         |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                          |
| tornado_http   | 98.1 ms                                                | 96.9 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 900 ms: 1.44x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.41x faster                                                           |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.39x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                           |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 596 ms: 1.28x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.5 ms: 1.04x faster                                                          |
| float          | 78.9 ms                                                | 76.4 ms: 1.03x faster                                                          |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                          |
| regex_compile  | 141 ms                                                 | 147 ms: 1.04x slower                                                           |
| regex_dna      | 205 ms                                                 | 219 ms: 1.07x slower                                                           |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                          |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                          |
| tomli_loads          | 2.30 sec                                               | 2.09 sec: 1.10x faster                                                         |
| pickle_pure_python   | 320 us                                                 | 311 us: 1.03x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 245 us: 1.01x slower                                                           |
| pickle_dict          | 34.6 us                                                | 36.0 us: 1.04x slower                                                          |
| xml_etree_process    | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                          |
| pickle               | 11.0 us                                                | 11.9 us: 1.09x slower                                                          |
| xml_etree_generate   | 81.1 ms                                                | 88.8 ms: 1.10x slower                                                          |
| pickle_list          | 4.59 us                                                | 5.04 us: 1.10x slower                                                          |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, unpickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                          |
| python_startup_no_site | 6.01 ms                                                | 9.56 ms: 1.59x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                          |
| genshi_xml      | 53.4 ms                                                | 55.8 ms: 1.04x slower                                                          |
| django_template | 33.5 ms                                                | 36.0 ms: 1.07x slower                                                          |
| genshi_text     | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 111 us: 4.69x faster                                                           |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.49x faster                                                          |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                           |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                         |
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 900 ms: 1.44x faster                                                           |
| pylint                     | 476 ms                                                 | 336 ms: 1.42x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.41x faster                                                           |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.39x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                           |
| comprehensions             | 23.6 us                                                | 18.4 us: 1.28x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 596 ms: 1.28x faster                                                           |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                                           |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                          |
| richards_super             | 61.9 ms                                                | 53.2 ms: 1.16x faster                                                          |
| chaos                      | 71.9 ms                                                | 63.4 ms: 1.13x faster                                                          |
| deltablue                  | 3.92 ms                                                | 3.53 ms: 1.11x faster                                                          |
| tomli_loads                | 2.30 sec                                               | 2.09 sec: 1.10x faster                                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.34 ms: 1.07x faster                                                          |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                                           |
| richards                   | 49.8 ms                                                | 47.2 ms: 1.06x faster                                                          |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.05x faster                                                          |
| djangocms                  | 33.5 us                                                | 32.0 us: 1.05x faster                                                          |
| raytrace                   | 309 ms                                                 | 296 ms: 1.04x faster                                                           |
| mdp                        | 2.77 sec                                               | 2.66 sec: 1.04x faster                                                         |
| nbody                      | 96.0 ms                                                | 92.5 ms: 1.04x faster                                                          |
| logging_simple             | 6.22 us                                                | 6.01 us: 1.04x faster                                                          |
| float                      | 78.9 ms                                                | 76.4 ms: 1.03x faster                                                          |
| pickle_pure_python         | 320 us                                                 | 311 us: 1.03x faster                                                           |
| logging_format             | 6.81 us                                                | 6.64 us: 1.03x faster                                                          |
| crypto_pyaes               | 76.7 ms                                                | 74.8 ms: 1.03x faster                                                          |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.03x faster                                                         |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                           |
| sympy_str                  | 297 ms                                                 | 291 ms: 1.02x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.95 ms: 1.01x faster                                                          |
| deepcopy                   | 365 us                                                 | 360 us: 1.01x faster                                                           |
| tornado_http               | 98.1 ms                                                | 96.9 ms: 1.01x faster                                                          |
| deepcopy_memo              | 40.2 us                                                | 39.7 us: 1.01x faster                                                          |
| scimark_fft                | 345 ms                                                 | 343 ms: 1.01x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 70.3 ms: 1.01x faster                                                          |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                           |
| unpickle_pure_python       | 242 us                                                 | 245 us: 1.01x slower                                                           |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.02x slower                                                          |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                          |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                          |
| sympy_expand               | 484 ms                                                 | 495 ms: 1.02x slower                                                           |
| nqueens                    | 87.9 ms                                                | 90.2 ms: 1.03x slower                                                          |
| json                       | 5.24 ms                                                | 5.40 ms: 1.03x slower                                                          |
| bench_thread_pool          | 834 us                                                 | 860 us: 1.03x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                          |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.03x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.04x slower                                                           |
| dask                       | 365 ms                                                 | 378 ms: 1.04x slower                                                           |
| pickle_dict                | 34.6 us                                                | 36.0 us: 1.04x slower                                                          |
| regex_compile              | 141 ms                                                 | 147 ms: 1.04x slower                                                           |
| go                         | 149 ms                                                 | 155 ms: 1.04x slower                                                           |
| genshi_xml                 | 53.4 ms                                                | 55.8 ms: 1.04x slower                                                          |
| chameleon                  | 6.70 ms                                                | 7.00 ms: 1.05x slower                                                          |
| sqlglot_optimize           | 55.3 ms                                                | 58.0 ms: 1.05x slower                                                          |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                          |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                           |
| hexiom                     | 6.89 ms                                                | 7.29 ms: 1.06x slower                                                          |
| thrift                     | 784 us                                                 | 831 us: 1.06x slower                                                           |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.06x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                          |
| regex_dna                  | 205 ms                                                 | 219 ms: 1.07x slower                                                           |
| django_template            | 33.5 ms                                                | 36.0 ms: 1.07x slower                                                          |
| docutils                   | 2.66 sec                                               | 2.89 sec: 1.09x slower                                                         |
| pickle                     | 11.0 us                                                | 11.9 us: 1.09x slower                                                          |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                                          |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                          |
| dulwich_log                | 64.6 ms                                                | 70.7 ms: 1.09x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 88.8 ms: 1.10x slower                                                          |
| pickle_list                | 4.59 us                                                | 5.04 us: 1.10x slower                                                          |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                           |
| genshi_text                | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                          |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                          |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                          |
| pyflate                    | 434 ms                                                 | 488 ms: 1.12x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                                          |
| scimark_lu                 | 116 ms                                                 | 133 ms: 1.14x slower                                                           |
| mypy2                      | 686 ms                                                 | 787 ms: 1.15x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.70 ms: 1.19x slower                                                          |
| async_generators           | 374 ms                                                 | 464 ms: 1.24x slower                                                           |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                          |
| telco                      | 6.86 ms                                                | 8.59 ms: 1.25x slower                                                          |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                          |
| python_startup_no_site     | 6.01 ms                                                | 9.56 ms: 1.59x slower                                                          |
| unpack_sequence            | 43.5 ns                                                | 85.5 ns: 1.97x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                   |

Benchmark hidden because not significant (10): xml_etree_parse, fannkuch, scimark_sparse_mat_mult, xml_etree_iterparse, deepcopy_reduce, unpickle_list, bench_mp_pool, pprint_safe_repr, json_loads, pycparser
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 62.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
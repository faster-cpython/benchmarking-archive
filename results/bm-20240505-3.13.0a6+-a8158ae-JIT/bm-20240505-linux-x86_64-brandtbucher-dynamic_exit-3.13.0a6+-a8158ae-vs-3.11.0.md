# Results vs. 3.11.0

- fork: brandtbucher
- ref: dynamic_exit
- machine: linux-x86_64
- commit hash: a8158ae
- commit date: 2024-05-05
- overall geometric mean: 1.05x faster
- HPT reliability: 93.69%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 284 ms: 1.07x slower                                                 |
| chameleon      | 6.70 ms                                                | 7.30 ms: 1.09x slower                                                |
| html5lib       | 64.8 ms                                                | 70.5 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 371 ms: 1.42x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 351 ms: 1.40x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 469 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 972 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 625 ms: 1.20x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 79.0 ms: 1.22x faster                                                |
| float          | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.11x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                         |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.29x faster                                                |
| tomli_loads          | 2.30 sec                                               | 1.97 sec: 1.17x faster                                               |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 153 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                 |
| json_loads           | 29.2 us                                                | 27.9 us: 1.04x faster                                                |
| pickle_dict          | 34.6 us                                                | 35.5 us: 1.03x slower                                                |
| unpickle_list        | 5.21 us                                                | 5.39 us: 1.03x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 58.9 ms: 1.03x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 84.2 ms: 1.04x slower                                                |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                |
| pickle_list          | 4.59 us                                                | 4.99 us: 1.09x slower                                                |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.66 ms: 1.27x slower                                                |
| python_startup         | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.67 ms: 1.10x faster                                                |
| django_template | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                |
| genshi_text     | 22.5 ms                                                | 24.5 ms: 1.09x slower                                                |
| genshi_xml      | 53.4 ms                                                | 58.2 ms: 1.09x slower                                                |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 175 us: 2.96x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 521 ms: 1.68x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                               |
| generators                 | 74.9 ms                                                | 51.4 ms: 1.46x faster                                                |
| async_tree_none            | 528 ms                                                 | 371 ms: 1.42x faster                                                 |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 351 ms: 1.40x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 469 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 972 ms: 1.33x faster                                                 |
| pylint                     | 476 ms                                                 | 364 ms: 1.31x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.29x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                 |
| richards_super             | 61.9 ms                                                | 49.3 ms: 1.26x faster                                                |
| chaos                      | 71.9 ms                                                | 58.2 ms: 1.23x faster                                                |
| nbody                      | 96.0 ms                                                | 79.0 ms: 1.22x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 625 ms: 1.20x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 1.97 sec: 1.17x faster                                               |
| richards                   | 49.8 ms                                                | 43.2 ms: 1.15x faster                                                |
| coroutines                 | 27.0 ms                                                | 23.7 ms: 1.14x faster                                                |
| fannkuch                   | 405 ms                                                 | 359 ms: 1.13x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 69.1 ms: 1.11x faster                                                |
| scimark_fft                | 345 ms                                                 | 313 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 64.2 ms: 1.10x faster                                                |
| mako                       | 10.7 ms                                                | 9.67 ms: 1.10x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                |
| raytrace                   | 309 ms                                                 | 282 ms: 1.09x faster                                                 |
| spectral_norm              | 108 ms                                                 | 99.0 ms: 1.09x faster                                                |
| float                      | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.63 ms: 1.09x faster                                                |
| logging_simple             | 6.22 us                                                | 5.75 us: 1.08x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 224 us: 1.08x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 153 ms: 1.07x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                               |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                 |
| deepcopy_memo              | 40.2 us                                                | 37.8 us: 1.06x faster                                                |
| logging_format             | 6.81 us                                                | 6.43 us: 1.06x faster                                                |
| json_loads                 | 29.2 us                                                | 27.9 us: 1.04x faster                                                |
| hexiom                     | 6.89 ms                                                | 6.60 ms: 1.04x faster                                                |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.04x faster                                                |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                               |
| djangocms                  | 33.5 us                                                | 32.6 us: 1.03x faster                                                |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 747 ms                                                 | 731 ms: 1.02x faster                                                 |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                               |
| logging_silent             | 111 ns                                                 | 109 ns: 1.02x faster                                                 |
| deltablue                  | 3.92 ms                                                | 3.86 ms: 1.02x faster                                                |
| go                         | 149 ms                                                 | 148 ms: 1.00x faster                                                 |
| nqueens                    | 87.9 ms                                                | 88.4 ms: 1.01x slower                                                |
| deepcopy                   | 365 us                                                 | 368 us: 1.01x slower                                                 |
| sympy_str                  | 297 ms                                                 | 302 ms: 1.02x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.30 us: 1.03x slower                                                |
| pickle_dict                | 34.6 us                                                | 35.5 us: 1.03x slower                                                |
| gc_traversal               | 4.01 ms                                                | 4.12 ms: 1.03x slower                                                |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 57.0 ms: 1.03x slower                                                |
| sqlglot_normalize          | 113 ms                                                 | 116 ms: 1.03x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.39 us: 1.03x slower                                                |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 58.9 ms: 1.03x slower                                                |
| dask                       | 365 ms                                                 | 378 ms: 1.04x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 84.2 ms: 1.04x slower                                                |
| pyflate                    | 434 ms                                                 | 452 ms: 1.04x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 871 us: 1.04x slower                                                 |
| sympy_expand               | 484 ms                                                 | 508 ms: 1.05x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 22.8 ms: 1.06x slower                                                |
| regex_effbot               | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                |
| django_template            | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                |
| 2to3                       | 264 ms                                                 | 284 ms: 1.07x slower                                                 |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                                 |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                |
| pickle_list                | 4.59 us                                                | 4.99 us: 1.09x slower                                                |
| html5lib                   | 64.8 ms                                                | 70.5 ms: 1.09x slower                                                |
| genshi_text                | 22.5 ms                                                | 24.5 ms: 1.09x slower                                                |
| genshi_xml                 | 53.4 ms                                                | 58.2 ms: 1.09x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.30 ms: 1.09x slower                                                |
| dulwich_log                | 64.6 ms                                                | 70.4 ms: 1.09x slower                                                |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.10x slower                                                 |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                                 |
| coverage                   | 78.8 ms                                                | 87.1 ms: 1.11x slower                                                |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.11x slower                                                |
| gunicorn                   | 1.20 ms                                                | 1.35 ms: 1.13x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                                |
| mypy2                      | 686 ms                                                 | 822 ms: 1.20x slower                                                 |
| telco                      | 6.86 ms                                                | 8.37 ms: 1.22x slower                                                |
| async_generators           | 374 ms                                                 | 465 ms: 1.24x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 9.25 ms: 1.27x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 7.66 ms: 1.27x slower                                                |
| python_startup             | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.87 ms: 1.31x slower                                                |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                         |

Benchmark hidden because not significant (5): json, regex_compile, tornado_http, bench_mp_pool, meteor_contest
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 93.69% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x
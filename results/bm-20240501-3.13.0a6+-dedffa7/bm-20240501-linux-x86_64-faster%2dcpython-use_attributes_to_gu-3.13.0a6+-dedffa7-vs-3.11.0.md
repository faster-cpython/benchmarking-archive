# Results vs. 3.11.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: dedffa7
- commit date: 2024-05-01
- overall geometric mean: 1.06x faster
- HPT reliability: 95.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.41 ms: 1.11x slower                                                            |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                            |
| tornado_http   | 98.1 ms                                                | 93.8 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 948 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.4 ms: 1.09x faster                                                            |
| pidigits       | 194 ms                                                 | 195 ms: 1.00x slower                                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                            |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                            |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.10x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 311 us: 1.03x faster                                                             |
| json_loads           | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| pickle_dict          | 34.6 us                                                | 35.9 us: 1.04x slower                                                            |
| pickle               | 11.0 us                                                | 11.6 us: 1.05x slower                                                            |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 62.3 ms: 1.09x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 90.3 ms: 1.11x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.12 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.3 ms: 1.04x faster                                                            |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                            |
| genshi_text     | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                            |
| mako            | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.16x faster                                                             |
| generators                 | 74.9 ms                                                | 29.2 ms: 2.56x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                             |
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 948 ms: 1.37x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.21x faster                                                            |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.6 ms: 1.19x faster                                                            |
| raytrace                   | 309 ms                                                 | 266 ms: 1.16x faster                                                             |
| richards_super             | 61.9 ms                                                | 55.6 ms: 1.11x faster                                                            |
| nqueens                    | 87.9 ms                                                | 79.6 ms: 1.10x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.10x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.33 ms: 1.09x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.61 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| nbody                      | 96.0 ms                                                | 88.4 ms: 1.09x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.57 sec: 1.08x faster                                                           |
| djangocms                  | 33.5 us                                                | 31.2 us: 1.08x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.79 us: 1.07x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                           |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                                            |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                             |
| pathlib                    | 18.5 ms                                                | 17.5 ms: 1.06x faster                                                            |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                            |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                             |
| tornado_http               | 98.1 ms                                                | 93.8 ms: 1.04x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 51.3 ms: 1.04x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 38.7 us: 1.04x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 311 us: 1.03x faster                                                             |
| sympy_expand               | 484 ms                                                 | 472 ms: 1.03x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                             |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                                             |
| richards                   | 49.8 ms                                                | 49.0 ms: 1.02x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 75.6 ms: 1.02x faster                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 70.0 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 826 us: 1.01x faster                                                             |
| fannkuch                   | 405 ms                                                 | 402 ms: 1.01x faster                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.98 ms: 1.01x faster                                                            |
| deepcopy                   | 365 us                                                 | 364 us: 1.00x faster                                                             |
| pidigits                   | 194 ms                                                 | 195 ms: 1.00x slower                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.23 us: 1.00x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 118 ms: 1.01x slower                                                             |
| pprint_safe_repr           | 747 ms                                                 | 761 ms: 1.02x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 65.9 ms: 1.02x slower                                                            |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                             |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| spectral_norm              | 108 ms                                                 | 111 ms: 1.03x slower                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.19 ms: 1.03x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.9 us: 1.04x slower                                                            |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                            |
| thrift                     | 784 us                                                 | 822 us: 1.05x slower                                                             |
| genshi_text                | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                            |
| pickle                     | 11.0 us                                                | 11.6 us: 1.05x slower                                                            |
| json                       | 5.24 ms                                                | 5.53 ms: 1.05x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| mako                       | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                            |
| mypy2                      | 686 ms                                                 | 737 ms: 1.08x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| scimark_fft                | 345 ms                                                 | 377 ms: 1.09x slower                                                             |
| xml_etree_process          | 56.9 ms                                                | 62.3 ms: 1.09x slower                                                            |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                             |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| chameleon                  | 6.70 ms                                                | 7.41 ms: 1.11x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 90.3 ms: 1.11x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.12 us: 1.12x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                            |
| pyflate                    | 434 ms                                                 | 489 ms: 1.13x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                            |
| async_generators           | 374 ms                                                 | 445 ms: 1.19x slower                                                             |
| coverage                   | 78.8 ms                                                | 93.8 ms: 1.19x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.52 ms: 1.24x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (4): sqlglot_optimize, pprint_pformat, float, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 95.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
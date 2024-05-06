# Results vs. base

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 6ccc646
- commit date: 2024-04-23
- overall geometric mean: 1.14x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 352 ms: 1.13x slower                                                             |
| chameleon      | 7.90 ms                                                                | 10.0 ms: 1.27x slower                                                            |
| docutils       | 3.18 sec                                                               | 3.61 sec: 1.14x slower                                                           |
| html5lib       | 71.6 ms                                                                | 103 ms: 1.44x slower                                                             |
| tornado_http   | 102 ms                                                                 | 136 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 630 ms                                                                 | 714 ms: 1.13x slower                                                             |
| async_tree_cpu_io_mixed    | 644 ms                                                                 | 734 ms: 1.14x slower                                                             |
| async_tree_io              | 976 ms                                                                 | 1.11 sec: 1.14x slower                                                           |
| async_tree_io_tg           | 993 ms                                                                 | 1.14 sec: 1.14x slower                                                           |
| async_tree_memoization     | 510 ms                                                                 | 608 ms: 1.19x slower                                                             |
| async_tree_none_tg         | 360 ms                                                                 | 429 ms: 1.19x slower                                                             |
| async_tree_none            | 383 ms                                                                 | 457 ms: 1.19x slower                                                             |
| async_tree_memoization_tg  | 468 ms                                                                 | 564 ms: 1.21x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 193 ms                                                                 | 194 ms: 1.00x slower                                                             |
| float          | 91.1 ms                                                                | 94.3 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 226 ms                                                                 | 227 ms: 1.00x slower                                                             |
| regex_effbot   | 3.69 ms                                                                | 3.72 ms: 1.01x slower                                                            |
| regex_compile  | 190 ms                                                                 | 231 ms: 1.22x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.14 us                                                                | 5.17 us: 1.00x slower                                                            |
| xml_etree_iterparse  | 111 ms                                                                 | 112 ms: 1.01x slower                                                             |
| unpickle_list        | 5.31 us                                                                | 5.42 us: 1.02x slower                                                            |
| pickle_dict          | 34.7 us                                                                | 35.4 us: 1.02x slower                                                            |
| json_loads           | 27.9 us                                                                | 28.5 us: 1.02x slower                                                            |
| pickle               | 11.6 us                                                                | 12.0 us: 1.04x slower                                                            |
| unpickle             | 15.1 us                                                                | 15.8 us: 1.05x slower                                                            |
| tomli_loads          | 2.67 sec                                                               | 2.99 sec: 1.12x slower                                                           |
| unpickle_pure_python | 297 us                                                                 | 337 us: 1.14x slower                                                             |
| xml_etree_generate   | 95.5 ms                                                                | 111 ms: 1.16x slower                                                             |
| json_dumps           | 10.8 ms                                                                | 12.7 ms: 1.17x slower                                                            |
| xml_etree_process    | 64.5 ms                                                                | 81.4 ms: 1.26x slower                                                            |
| pickle_pure_python   | 314 us                                                                 | 500 us: 1.59x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                                     |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                                | 7.18 ms: 1.00x slower                                                            |
| python_startup         | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 13.1 ms                                                                | 13.8 ms: 1.05x slower                                                            |
| genshi_xml      | 61.7 ms                                                                | 74.2 ms: 1.20x slower                                                            |
| genshi_text     | 26.0 ms                                                                | 32.4 ms: 1.25x slower                                                            |
| django_template | 42.8 ms                                                                | 60.9 ms: 1.42x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| scimark_monte_carlo        | 103 ms                                                                 | 93.1 ms: 1.11x faster                                                            |
| crypto_pyaes               | 103 ms                                                                 | 93.4 ms: 1.10x faster                                                            |
| pyflate                    | 712 ms                                                                 | 652 ms: 1.09x faster                                                             |
| fannkuch                   | 524 ms                                                                 | 505 ms: 1.04x faster                                                             |
| meteor_contest             | 125 ms                                                                 | 123 ms: 1.01x faster                                                             |
| pidigits                   | 193 ms                                                                 | 194 ms: 1.00x slower                                                             |
| python_startup_no_site     | 7.16 ms                                                                | 7.18 ms: 1.00x slower                                                            |
| regex_dna                  | 226 ms                                                                 | 227 ms: 1.00x slower                                                             |
| pickle_list                | 5.14 us                                                                | 5.17 us: 1.00x slower                                                            |
| asyncio_websockets         | 567 ms                                                                 | 571 ms: 1.01x slower                                                             |
| python_startup             | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                            |
| regex_effbot               | 3.69 ms                                                                | 3.72 ms: 1.01x slower                                                            |
| xml_etree_iterparse        | 111 ms                                                                 | 112 ms: 1.01x slower                                                             |
| scimark_fft                | 452 ms                                                                 | 458 ms: 1.01x slower                                                             |
| create_gc_cycles           | 1.77 ms                                                                | 1.80 ms: 1.02x slower                                                            |
| comprehensions             | 24.7 us                                                                | 25.2 us: 1.02x slower                                                            |
| unpickle_list              | 5.31 us                                                                | 5.42 us: 1.02x slower                                                            |
| pickle_dict                | 34.7 us                                                                | 35.4 us: 1.02x slower                                                            |
| json_loads                 | 27.9 us                                                                | 28.5 us: 1.02x slower                                                            |
| scimark_sparse_mat_mult    | 6.05 ms                                                                | 6.19 ms: 1.02x slower                                                            |
| sqlite_synth               | 3.09 us                                                                | 3.16 us: 1.02x slower                                                            |
| spectral_norm              | 140 ms                                                                 | 144 ms: 1.03x slower                                                             |
| asyncio_tcp_ssl            | 1.86 sec                                                               | 1.91 sec: 1.03x slower                                                           |
| async_generators           | 489 ms                                                                 | 504 ms: 1.03x slower                                                             |
| json                       | 5.26 ms                                                                | 5.42 ms: 1.03x slower                                                            |
| float                      | 91.1 ms                                                                | 94.3 ms: 1.04x slower                                                            |
| pickle                     | 11.6 us                                                                | 12.0 us: 1.04x slower                                                            |
| bench_mp_pool              | 24.0 ms                                                                | 25.0 ms: 1.04x slower                                                            |
| unpickle                   | 15.1 us                                                                | 15.8 us: 1.05x slower                                                            |
| mako                       | 13.1 ms                                                                | 13.8 ms: 1.05x slower                                                            |
| generators                 | 30.2 ms                                                                | 31.7 ms: 1.05x slower                                                            |
| mdp                        | 2.83 sec                                                               | 2.99 sec: 1.06x slower                                                           |
| hexiom                     | 10.2 ms                                                                | 10.8 ms: 1.06x slower                                                            |
| gc_traversal               | 3.76 ms                                                                | 4.03 ms: 1.07x slower                                                            |
| nqueens                    | 129 ms                                                                 | 139 ms: 1.08x slower                                                             |
| coroutines                 | 23.3 ms                                                                | 25.5 ms: 1.10x slower                                                            |
| bench_thread_pool          | 904 us                                                                 | 998 us: 1.10x slower                                                             |
| asyncio_tcp                | 514 ms                                                                 | 569 ms: 1.11x slower                                                             |
| pathlib                    | 18.7 ms                                                                | 20.8 ms: 1.11x slower                                                            |
| deepcopy_memo              | 49.3 us                                                                | 55.0 us: 1.12x slower                                                            |
| djangocms                  | 32.7 us                                                                | 36.5 us: 1.12x slower                                                            |
| tomli_loads                | 2.67 sec                                                               | 2.99 sec: 1.12x slower                                                           |
| scimark_lu                 | 170 ms                                                                 | 190 ms: 1.12x slower                                                             |
| async_tree_cpu_io_mixed_tg | 630 ms                                                                 | 714 ms: 1.13x slower                                                             |
| 2to3                       | 310 ms                                                                 | 352 ms: 1.13x slower                                                             |
| unpickle_pure_python       | 297 us                                                                 | 337 us: 1.14x slower                                                             |
| docutils                   | 3.18 sec                                                               | 3.61 sec: 1.14x slower                                                           |
| pprint_pformat             | 2.27 sec                                                               | 2.58 sec: 1.14x slower                                                           |
| pprint_safe_repr           | 1.09 sec                                                               | 1.24 sec: 1.14x slower                                                           |
| async_tree_cpu_io_mixed    | 644 ms                                                                 | 734 ms: 1.14x slower                                                             |
| async_tree_io              | 976 ms                                                                 | 1.11 sec: 1.14x slower                                                           |
| async_tree_io_tg           | 993 ms                                                                 | 1.14 sec: 1.14x slower                                                           |
| xml_etree_generate         | 95.5 ms                                                                | 111 ms: 1.16x slower                                                             |
| json_dumps                 | 10.8 ms                                                                | 12.7 ms: 1.17x slower                                                            |
| sympy_sum                  | 184 ms                                                                 | 216 ms: 1.18x slower                                                             |
| sympy_integrate            | 24.1 ms                                                                | 28.3 ms: 1.18x slower                                                            |
| async_tree_memoization     | 510 ms                                                                 | 608 ms: 1.19x slower                                                             |
| async_tree_none_tg         | 360 ms                                                                 | 429 ms: 1.19x slower                                                             |
| async_tree_none            | 383 ms                                                                 | 457 ms: 1.19x slower                                                             |
| go                         | 193 ms                                                                 | 230 ms: 1.20x slower                                                             |
| richards_super             | 70.7 ms                                                                | 84.5 ms: 1.20x slower                                                            |
| pylint                     | 348 ms                                                                 | 416 ms: 1.20x slower                                                             |
| scimark_sor                | 166 ms                                                                 | 199 ms: 1.20x slower                                                             |
| gunicorn                   | 1.34 ms                                                                | 1.61 ms: 1.20x slower                                                            |
| aiohttp                    | 1.25 ms                                                                | 1.50 ms: 1.20x slower                                                            |
| genshi_xml                 | 61.7 ms                                                                | 74.2 ms: 1.20x slower                                                            |
| async_tree_memoization_tg  | 468 ms                                                                 | 564 ms: 1.21x slower                                                             |
| sympy_str                  | 334 ms                                                                 | 403 ms: 1.21x slower                                                             |
| chaos                      | 85.4 ms                                                                | 103 ms: 1.21x slower                                                             |
| typing_runtime_protocols   | 127 us                                                                 | 154 us: 1.21x slower                                                             |
| sqlglot_optimize           | 67.1 ms                                                                | 81.2 ms: 1.21x slower                                                            |
| mypy2                      | 820 ms                                                                 | 994 ms: 1.21x slower                                                             |
| richards                   | 62.6 ms                                                                | 76.0 ms: 1.21x slower                                                            |
| regex_compile              | 190 ms                                                                 | 231 ms: 1.22x slower                                                             |
| pycparser                  | 1.31 sec                                                               | 1.61 sec: 1.23x slower                                                           |
| sympy_expand               | 548 ms                                                                 | 679 ms: 1.24x slower                                                             |
| genshi_text                | 26.0 ms                                                                | 32.4 ms: 1.25x slower                                                            |
| dask                       | 383 ms                                                                 | 481 ms: 1.26x slower                                                             |
| dulwich_log                | 74.6 ms                                                                | 93.7 ms: 1.26x slower                                                            |
| xml_etree_process          | 64.5 ms                                                                | 81.4 ms: 1.26x slower                                                            |
| chameleon                  | 7.90 ms                                                                | 10.0 ms: 1.27x slower                                                            |
| thrift                     | 842 us                                                                 | 1.08 ms: 1.28x slower                                                            |
| sqlglot_normalize          | 128 ms                                                                 | 166 ms: 1.29x slower                                                             |
| sqlglot_parse              | 1.55 ms                                                                | 2.04 ms: 1.32x slower                                                            |
| tornado_http               | 102 ms                                                                 | 136 ms: 1.32x slower                                                             |
| sqlglot_transpile          | 1.87 ms                                                                | 2.52 ms: 1.34x slower                                                            |
| raytrace                   | 350 ms                                                                 | 474 ms: 1.35x slower                                                             |
| logging_silent             | 106 ns                                                                 | 147 ns: 1.38x slower                                                             |
| django_template            | 42.8 ms                                                                | 60.9 ms: 1.42x slower                                                            |
| deepcopy                   | 387 us                                                                 | 553 us: 1.43x slower                                                             |
| deltablue                  | 4.39 ms                                                                | 6.30 ms: 1.43x slower                                                            |
| html5lib                   | 71.6 ms                                                                | 103 ms: 1.44x slower                                                             |
| deepcopy_reduce            | 3.30 us                                                                | 5.09 us: 1.54x slower                                                            |
| logging_format             | 7.34 us                                                                | 11.7 us: 1.59x slower                                                            |
| pickle_pure_python         | 314 us                                                                 | 500 us: 1.59x slower                                                             |
| logging_simple             | 6.56 us                                                                | 10.5 us: 1.61x slower                                                            |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                                     |

Benchmark hidden because not significant (5): nbody, regex_v8, telco, coverage, xml_etree_parse

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.00x
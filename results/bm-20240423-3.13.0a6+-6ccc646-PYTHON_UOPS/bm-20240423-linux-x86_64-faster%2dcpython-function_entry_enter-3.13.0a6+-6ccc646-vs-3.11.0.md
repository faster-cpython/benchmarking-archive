# Results vs. 3.11.0

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 6ccc646
- commit date: 2024-04-23
- overall geometric mean: 1.21x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 352 ms: 1.33x slower                                                             |
| chameleon      | 6.70 ms                                                | 10.0 ms: 1.50x slower                                                            |
| docutils       | 2.66 sec                                               | 3.61 sec: 1.36x slower                                                           |
| html5lib       | 64.8 ms                                                | 103 ms: 1.59x slower                                                             |
| tornado_http   | 98.1 ms                                                | 136 ms: 1.38x slower                                                             |
| Geometric mean | (ref)                                                  | 1.43x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 1.29 sec                                               | 1.11 sec: 1.16x faster                                                           |
| async_tree_none            | 528 ms                                                 | 457 ms: 1.16x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 429 ms: 1.15x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1.14 sec: 1.14x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 564 ms: 1.11x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 714 ms: 1.07x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 608 ms: 1.05x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 734 ms: 1.02x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                                             |
| float          | 78.9 ms                                                | 94.3 ms: 1.20x slower                                                            |
| nbody          | 96.0 ms                                                | 122 ms: 1.28x slower                                                             |
| Geometric mean | (ref)                                                  | 1.15x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.72 ms: 1.06x slower                                                            |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                            |
| regex_compile  | 141 ms                                                 | 231 ms: 1.64x slower                                                             |
| Geometric mean | (ref)                                                  | 1.21x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 164 ms                                                 | 155 ms: 1.06x faster                                                             |
| json_dumps           | 13.3 ms                                                | 12.7 ms: 1.05x faster                                                            |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                                            |
| unpickle_list        | 5.21 us                                                | 5.42 us: 1.04x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 112 ms: 1.04x slower                                                             |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.17 us: 1.13x slower                                                            |
| unpickle             | 13.8 us                                                | 15.8 us: 1.14x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.99 sec: 1.30x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 111 ms: 1.37x slower                                                             |
| unpickle_pure_python | 242 us                                                 | 337 us: 1.39x slower                                                             |
| xml_etree_process    | 56.9 ms                                                | 81.4 ms: 1.43x slower                                                            |
| pickle_pure_python   | 320 us                                                 | 500 us: 1.56x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.16x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.18 ms: 1.19x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.24x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 13.8 ms: 1.29x slower                                                            |
| genshi_xml      | 53.4 ms                                                | 74.2 ms: 1.39x slower                                                            |
| genshi_text     | 22.5 ms                                                | 32.4 ms: 1.44x slower                                                            |
| django_template | 33.5 ms                                                | 60.9 ms: 1.82x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.47x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 154 us: 3.37x faster                                                             |
| generators                 | 74.9 ms                                                | 31.7 ms: 2.36x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.91 sec: 1.62x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 569 ms: 1.54x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 1.11 sec: 1.16x faster                                                           |
| async_tree_none            | 528 ms                                                 | 457 ms: 1.16x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 429 ms: 1.15x faster                                                             |
| pylint                     | 476 ms                                                 | 416 ms: 1.14x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1.14 sec: 1.14x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 564 ms: 1.11x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 714 ms: 1.07x faster                                                             |
| coroutines                 | 27.0 ms                                                | 25.5 ms: 1.06x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 155 ms: 1.06x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 608 ms: 1.05x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 12.7 ms: 1.05x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 734 ms: 1.02x faster                                                             |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                                             |
| gc_traversal               | 4.01 ms                                                | 4.03 ms: 1.01x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.4 us: 1.02x slower                                                            |
| json                       | 5.24 ms                                                | 5.42 ms: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 571 ms: 1.04x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.42 us: 1.04x slower                                                            |
| bench_mp_pool              | 24.0 ms                                                | 25.0 ms: 1.04x slower                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 112 ms: 1.04x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.72 ms: 1.06x slower                                                            |
| comprehensions             | 23.6 us                                                | 25.2 us: 1.07x slower                                                            |
| mdp                        | 2.77 sec                                               | 2.99 sec: 1.08x slower                                                           |
| djangocms                  | 33.5 us                                                | 36.5 us: 1.09x slower                                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                            |
| pathlib                    | 18.5 ms                                                | 20.8 ms: 1.12x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.17 us: 1.13x slower                                                            |
| meteor_contest             | 109 ms                                                 | 123 ms: 1.13x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.8 us: 1.14x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.18 ms: 1.19x slower                                                            |
| float                      | 78.9 ms                                                | 94.3 ms: 1.20x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 998 us: 1.20x slower                                                             |
| crypto_pyaes               | 76.7 ms                                                | 93.4 ms: 1.22x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 3.16 us: 1.23x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.19 ms: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.24x slower                                                            |
| fannkuch                   | 405 ms                                                 | 505 ms: 1.25x slower                                                             |
| coverage                   | 78.8 ms                                                | 98.5 ms: 1.25x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                            |
| nbody                      | 96.0 ms                                                | 122 ms: 1.28x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 216 ms: 1.28x slower                                                             |
| mako                       | 10.7 ms                                                | 13.8 ms: 1.29x slower                                                            |
| tomli_loads                | 2.30 sec                                               | 2.99 sec: 1.30x slower                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 93.1 ms: 1.32x slower                                                            |
| sympy_integrate            | 21.5 ms                                                | 28.3 ms: 1.32x slower                                                            |
| dask                       | 365 ms                                                 | 481 ms: 1.32x slower                                                             |
| logging_silent             | 111 ns                                                 | 147 ns: 1.33x slower                                                             |
| scimark_fft                | 345 ms                                                 | 458 ms: 1.33x slower                                                             |
| spectral_norm              | 108 ms                                                 | 144 ms: 1.33x slower                                                             |
| 2to3                       | 264 ms                                                 | 352 ms: 1.33x slower                                                             |
| gunicorn                   | 1.20 ms                                                | 1.61 ms: 1.34x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.50 ms: 1.35x slower                                                            |
| async_generators           | 374 ms                                                 | 504 ms: 1.35x slower                                                             |
| sympy_str                  | 297 ms                                                 | 403 ms: 1.36x slower                                                             |
| docutils                   | 2.66 sec                                               | 3.61 sec: 1.36x slower                                                           |
| pycparser                  | 1.19 sec                                               | 1.61 sec: 1.36x slower                                                           |
| richards_super             | 61.9 ms                                                | 84.5 ms: 1.37x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 111 ms: 1.37x slower                                                             |
| deepcopy_memo              | 40.2 us                                                | 55.0 us: 1.37x slower                                                            |
| thrift                     | 784 us                                                 | 1.08 ms: 1.37x slower                                                            |
| tornado_http               | 98.1 ms                                                | 136 ms: 1.38x slower                                                             |
| genshi_xml                 | 53.4 ms                                                | 74.2 ms: 1.39x slower                                                            |
| unpickle_pure_python       | 242 us                                                 | 337 us: 1.39x slower                                                             |
| sympy_expand               | 484 ms                                                 | 679 ms: 1.40x slower                                                             |
| telco                      | 6.86 ms                                                | 9.65 ms: 1.41x slower                                                            |
| sqlglot_parse              | 1.43 ms                                                | 2.04 ms: 1.42x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 81.4 ms: 1.43x slower                                                            |
| chaos                      | 71.9 ms                                                | 103 ms: 1.43x slower                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 2.52 ms: 1.44x slower                                                            |
| genshi_text                | 22.5 ms                                                | 32.4 ms: 1.44x slower                                                            |
| mypy2                      | 686 ms                                                 | 994 ms: 1.45x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 93.7 ms: 1.45x slower                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 81.2 ms: 1.47x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 166 ms: 1.47x slower                                                             |
| chameleon                  | 6.70 ms                                                | 10.0 ms: 1.50x slower                                                            |
| pyflate                    | 434 ms                                                 | 652 ms: 1.50x slower                                                             |
| deepcopy                   | 365 us                                                 | 553 us: 1.51x slower                                                             |
| richards                   | 49.8 ms                                                | 76.0 ms: 1.53x slower                                                            |
| raytrace                   | 309 ms                                                 | 474 ms: 1.53x slower                                                             |
| go                         | 149 ms                                                 | 230 ms: 1.55x slower                                                             |
| pickle_pure_python         | 320 us                                                 | 500 us: 1.56x slower                                                             |
| hexiom                     | 6.89 ms                                                | 10.8 ms: 1.57x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 5.09 us: 1.58x slower                                                            |
| nqueens                    | 87.9 ms                                                | 139 ms: 1.59x slower                                                             |
| html5lib                   | 64.8 ms                                                | 103 ms: 1.59x slower                                                             |
| deltablue                  | 3.92 ms                                                | 6.30 ms: 1.61x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 190 ms: 1.63x slower                                                             |
| scimark_sor                | 121 ms                                                 | 199 ms: 1.64x slower                                                             |
| regex_compile              | 141 ms                                                 | 231 ms: 1.64x slower                                                             |
| pprint_pformat             | 1.55 sec                                               | 2.58 sec: 1.66x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 1.24 sec: 1.66x slower                                                           |
| logging_simple             | 6.22 us                                                | 10.5 us: 1.70x slower                                                            |
| logging_format             | 6.81 us                                                | 11.7 us: 1.71x slower                                                            |
| django_template            | 33.5 ms                                                | 60.9 ms: 1.82x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.21x slower                                                                     |
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.04x
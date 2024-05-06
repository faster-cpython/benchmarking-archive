# Results vs. 3.11.0

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: d04d9ac
- commit date: 2024-04-23
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 306 ms: 1.16x slower                                                             |
| chameleon      | 6.70 ms                                                | 8.10 ms: 1.21x slower                                                            |
| docutils       | 2.66 sec                                               | 3.13 sec: 1.17x slower                                                           |
| html5lib       | 64.8 ms                                                | 73.3 ms: 1.13x slower                                                            |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.05x slower                                                             |
| Geometric mean | (ref)                                                  | 1.14x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 356 ms: 1.38x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 467 ms: 1.34x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 971 ms: 1.33x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 975 ms: 1.32x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 508 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 626 ms: 1.22x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 199 ms: 1.03x slower                                                             |
| float          | 78.9 ms                                                | 94.9 ms: 1.20x slower                                                            |
| nbody          | 96.0 ms                                                | 128 ms: 1.33x slower                                                             |
| Geometric mean | (ref)                                                  | 1.18x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                            |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                            |
| regex_compile  | 141 ms                                                 | 186 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                  | 1.14x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                             |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 321 us: 1.00x slower                                                             |
| pickle_dict          | 34.6 us                                                | 35.5 us: 1.03x slower                                                            |
| unpickle_list        | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 114 ms: 1.06x slower                                                             |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| unpickle             | 13.8 us                                                | 15.3 us: 1.10x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.08 us: 1.11x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.62 sec: 1.14x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 65.6 ms: 1.15x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 95.3 ms: 1.18x slower                                                            |
| unpickle_pure_python | 242 us                                                 | 298 us: 1.23x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.14 ms: 1.19x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 59.9 ms: 1.12x slower                                                            |
| genshi_text     | 22.5 ms                                                | 25.7 ms: 1.14x slower                                                            |
| django_template | 33.5 ms                                                | 41.5 ms: 1.24x slower                                                            |
| mako            | 10.7 ms                                                | 14.5 ms: 1.36x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 128 us: 4.07x faster                                                             |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 528 ms: 1.66x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.88 sec: 1.66x faster                                                           |
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 356 ms: 1.38x faster                                                             |
| pylint                     | 476 ms                                                 | 351 ms: 1.36x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 467 ms: 1.34x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 971 ms: 1.33x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 975 ms: 1.32x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 508 ms: 1.26x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 626 ms: 1.22x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                             |
| coroutines                 | 27.0 ms                                                | 24.2 ms: 1.12x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                             |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                                            |
| djangocms                  | 33.5 us                                                | 33.0 us: 1.02x faster                                                            |
| logging_silent             | 111 ns                                                 | 110 ns: 1.01x faster                                                             |
| gc_traversal               | 4.01 ms                                                | 3.96 ms: 1.01x faster                                                            |
| pathlib                    | 18.5 ms                                                | 18.4 ms: 1.01x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 321 us: 1.00x slower                                                             |
| pickle_dict                | 34.6 us                                                | 35.5 us: 1.03x slower                                                            |
| pidigits                   | 194 ms                                                 | 199 ms: 1.03x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| richards_super             | 61.9 ms                                                | 63.7 ms: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                             |
| logging_simple             | 6.22 us                                                | 6.43 us: 1.03x slower                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.82 ms: 1.04x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.35 us: 1.04x slower                                                            |
| comprehensions             | 23.6 us                                                | 24.6 us: 1.04x slower                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.50 ms: 1.05x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                            |
| logging_format             | 6.81 us                                                | 7.16 us: 1.05x slower                                                            |
| deepcopy                   | 365 us                                                 | 384 us: 1.05x slower                                                             |
| dask                       | 365 ms                                                 | 384 ms: 1.05x slower                                                             |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.05x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.05x slower                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 114 ms: 1.06x slower                                                             |
| bench_thread_pool          | 834 us                                                 | 892 us: 1.07x slower                                                             |
| raytrace                   | 309 ms                                                 | 330 ms: 1.07x slower                                                             |
| thrift                     | 784 us                                                 | 841 us: 1.07x slower                                                             |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.29 sec: 1.09x slower                                                           |
| mdp                        | 2.77 sec                                               | 3.02 sec: 1.09x slower                                                           |
| deltablue                  | 3.92 ms                                                | 4.33 ms: 1.10x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.10x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.32 ms: 1.10x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.08 us: 1.11x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.23 ms: 1.11x slower                                                            |
| sympy_str                  | 297 ms                                                 | 330 ms: 1.11x slower                                                             |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 126 ms: 1.12x slower                                                             |
| genshi_xml                 | 53.4 ms                                                | 59.9 ms: 1.12x slower                                                            |
| meteor_contest             | 109 ms                                                 | 122 ms: 1.12x slower                                                             |
| sympy_integrate            | 21.5 ms                                                | 24.1 ms: 1.12x slower                                                            |
| chaos                      | 71.9 ms                                                | 80.9 ms: 1.13x slower                                                            |
| html5lib                   | 64.8 ms                                                | 73.3 ms: 1.13x slower                                                            |
| tomli_loads                | 2.30 sec                                               | 2.62 sec: 1.14x slower                                                           |
| genshi_text                | 22.5 ms                                                | 25.7 ms: 1.14x slower                                                            |
| sympy_expand               | 484 ms                                                 | 552 ms: 1.14x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 73.9 ms: 1.14x slower                                                            |
| deepcopy_memo              | 40.2 us                                                | 46.1 us: 1.15x slower                                                            |
| richards                   | 49.8 ms                                                | 57.3 ms: 1.15x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 65.6 ms: 1.15x slower                                                            |
| 2to3                       | 264 ms                                                 | 306 ms: 1.16x slower                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 64.5 ms: 1.17x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 3.01 us: 1.17x slower                                                            |
| docutils                   | 2.66 sec                                               | 3.13 sec: 1.17x slower                                                           |
| xml_etree_generate         | 81.1 ms                                                | 95.3 ms: 1.18x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.14 ms: 1.19x slower                                                            |
| mypy2                      | 686 ms                                                 | 821 ms: 1.20x slower                                                             |
| float                      | 78.9 ms                                                | 94.9 ms: 1.20x slower                                                            |
| chameleon                  | 6.70 ms                                                | 8.10 ms: 1.21x slower                                                            |
| unpickle_pure_python       | 242 us                                                 | 298 us: 1.23x slower                                                             |
| coverage                   | 78.8 ms                                                | 97.4 ms: 1.24x slower                                                            |
| django_template            | 33.5 ms                                                | 41.5 ms: 1.24x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| crypto_pyaes               | 76.7 ms                                                | 95.3 ms: 1.24x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                            |
| fannkuch                   | 405 ms                                                 | 511 ms: 1.26x slower                                                             |
| nqueens                    | 87.9 ms                                                | 111 ms: 1.27x slower                                                             |
| async_generators           | 374 ms                                                 | 482 ms: 1.29x slower                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.54 ms: 1.30x slower                                                            |
| pprint_pformat             | 1.55 sec                                               | 2.04 sec: 1.31x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 983 ms: 1.32x slower                                                             |
| regex_compile              | 141 ms                                                 | 186 ms: 1.32x slower                                                             |
| scimark_sor                | 121 ms                                                 | 161 ms: 1.33x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 93.9 ms: 1.33x slower                                                            |
| nbody                      | 96.0 ms                                                | 128 ms: 1.33x slower                                                             |
| go                         | 149 ms                                                 | 201 ms: 1.35x slower                                                             |
| mako                       | 10.7 ms                                                | 14.5 ms: 1.36x slower                                                            |
| telco                      | 6.86 ms                                                | 9.36 ms: 1.37x slower                                                            |
| scimark_fft                | 345 ms                                                 | 473 ms: 1.37x slower                                                             |
| spectral_norm              | 108 ms                                                 | 153 ms: 1.42x slower                                                             |
| hexiom                     | 6.89 ms                                                | 10.1 ms: 1.46x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 170 ms: 1.46x slower                                                             |
| pyflate                    | 434 ms                                                 | 639 ms: 1.47x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                                     |

Benchmark hidden because not significant (2): json, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.04x
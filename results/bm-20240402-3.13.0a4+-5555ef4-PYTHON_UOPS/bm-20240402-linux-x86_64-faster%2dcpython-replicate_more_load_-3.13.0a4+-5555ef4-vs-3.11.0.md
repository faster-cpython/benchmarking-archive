# Results vs. 3.11.0

- fork: faster-cpython
- ref: replicate_more_load_
- machine: linux-x86_64
- commit hash: 5555ef4
- commit date: 2024-04-02
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 300 ms: 1.14x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.08 ms: 1.06x slower                                                            |
| docutils       | 2.66 sec                                               | 2.87 sec: 1.08x slower                                                           |
| html5lib       | 64.8 ms                                                | 71.1 ms: 1.10x slower                                                            |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.05x slower                                                             |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|---------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none           | 528 ms                                                 | 463 ms: 1.14x faster                                                             |
| async_tree_memoization    | 639 ms                                                 | 594 ms: 1.07x faster                                                             |
| async_tree_none_tg        | 491 ms                                                 | 471 ms: 1.04x faster                                                             |
| async_tree_memoization_tg | 626 ms                                                 | 603 ms: 1.04x faster                                                             |
| async_tree_io             | 1.29 sec                                               | 1.24 sec: 1.04x faster                                                           |
| async_tree_io_tg          | 1.29 sec                                               | 1.26 sec: 1.03x faster                                                           |
| Geometric mean            | (ref)                                                  | 1.05x faster                                                                     |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 94.7 ms: 1.20x slower                                                            |
| nbody          | 96.0 ms                                                | 123 ms: 1.28x slower                                                             |
| Geometric mean | (ref)                                                  | 1.15x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                            |
| regex_dna      | 205 ms                                                 | 213 ms: 1.04x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                            |
| regex_compile  | 141 ms                                                 | 178 ms: 1.26x slower                                                             |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| json_loads           | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.12 us: 1.02x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 314 us: 1.02x faster                                                             |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| pickle_dict          | 34.6 us                                                | 34.9 us: 1.01x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 113 ms: 1.04x slower                                                             |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 62.8 ms: 1.10x slower                                                            |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 91.6 ms: 1.13x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.25 us: 1.14x slower                                                            |
| unpickle_pure_python | 242 us                                                 | 278 us: 1.15x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 9.07 ms: 1.51x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                            |
| mako            | 10.7 ms                                                | 12.9 ms: 1.21x slower                                                            |
| genshi_xml      | 53.4 ms                                                | 64.9 ms: 1.21x slower                                                            |
| genshi_text     | 22.5 ms                                                | 28.0 ms: 1.24x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.17x slower                                                                     |

All benchmarks:
===============

| Benchmark                 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|---------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols  | 520 us                                                 | 118 us: 4.40x faster                                                             |
| generators                | 74.9 ms                                                | 30.4 ms: 2.46x faster                                                            |
| asyncio_tcp               | 875 ms                                                 | 510 ms: 1.72x faster                                                             |
| asyncio_tcp_ssl           | 3.11 sec                                               | 1.86 sec: 1.68x faster                                                           |
| pylint                    | 476 ms                                                 | 333 ms: 1.43x faster                                                             |
| json_dumps                | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| async_tree_none           | 528 ms                                                 | 463 ms: 1.14x faster                                                             |
| comprehensions            | 23.6 us                                                | 20.9 us: 1.13x faster                                                            |
| coroutines                | 27.0 ms                                                | 24.0 ms: 1.13x faster                                                            |
| async_tree_memoization    | 639 ms                                                 | 594 ms: 1.07x faster                                                             |
| logging_silent            | 111 ns                                                 | 104 ns: 1.07x faster                                                             |
| async_tree_none_tg        | 491 ms                                                 | 471 ms: 1.04x faster                                                             |
| gc_traversal              | 4.01 ms                                                | 3.85 ms: 1.04x faster                                                            |
| async_tree_memoization_tg | 626 ms                                                 | 603 ms: 1.04x faster                                                             |
| async_tree_io             | 1.29 sec                                               | 1.24 sec: 1.04x faster                                                           |
| djangocms                 | 33.5 us                                                | 32.4 us: 1.03x faster                                                            |
| deepcopy_reduce           | 3.22 us                                                | 3.11 us: 1.03x faster                                                            |
| json_loads                | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| async_tree_io_tg          | 1.29 sec                                               | 1.26 sec: 1.03x faster                                                           |
| unpickle_list             | 5.21 us                                                | 5.12 us: 1.02x faster                                                            |
| pickle_pure_python        | 320 us                                                 | 314 us: 1.02x faster                                                             |
| xml_etree_parse           | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| pidigits                  | 194 ms                                                 | 191 ms: 1.02x faster                                                             |
| sympy_sum                 | 169 ms                                                 | 166 ms: 1.02x faster                                                             |
| deltablue                 | 3.92 ms                                                | 3.88 ms: 1.01x faster                                                            |
| mdp                       | 2.77 sec                                               | 2.75 sec: 1.01x faster                                                           |
| bench_mp_pool             | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                            |
| sympy_integrate           | 21.5 ms                                                | 21.5 ms: 1.00x slower                                                            |
| sqlglot_normalize         | 113 ms                                                 | 113 ms: 1.01x slower                                                             |
| pickle_dict               | 34.6 us                                                | 34.9 us: 1.01x slower                                                            |
| regex_effbot              | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                            |
| richards_super            | 61.9 ms                                                | 63.0 ms: 1.02x slower                                                            |
| json                      | 5.24 ms                                                | 5.35 ms: 1.02x slower                                                            |
| sqlglot_parse             | 1.43 ms                                                | 1.47 ms: 1.02x slower                                                            |
| logging_simple            | 6.22 us                                                | 6.37 us: 1.02x slower                                                            |
| asyncio_websockets        | 550 ms                                                 | 564 ms: 1.02x slower                                                             |
| django_template           | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                            |
| sympy_str                 | 297 ms                                                 | 306 ms: 1.03x slower                                                             |
| sqlglot_transpile         | 1.75 ms                                                | 1.81 ms: 1.03x slower                                                            |
| dask                      | 365 ms                                                 | 379 ms: 1.04x slower                                                             |
| pathlib                   | 18.5 ms                                                | 19.3 ms: 1.04x slower                                                            |
| regex_dna                 | 205 ms                                                 | 213 ms: 1.04x slower                                                             |
| xml_etree_iterparse       | 108 ms                                                 | 113 ms: 1.04x slower                                                             |
| chaos                     | 71.9 ms                                                | 75.2 ms: 1.05x slower                                                            |
| bench_thread_pool         | 834 us                                                 | 873 us: 1.05x slower                                                             |
| deepcopy_memo             | 40.2 us                                                | 42.2 us: 1.05x slower                                                            |
| tornado_http              | 98.1 ms                                                | 103 ms: 1.05x slower                                                             |
| logging_format            | 6.81 us                                                | 7.19 us: 1.06x slower                                                            |
| chameleon                 | 6.70 ms                                                | 7.08 ms: 1.06x slower                                                            |
| sympy_expand              | 484 ms                                                 | 514 ms: 1.06x slower                                                             |
| thrift                    | 784 us                                                 | 834 us: 1.06x slower                                                             |
| meteor_contest            | 109 ms                                                 | 117 ms: 1.08x slower                                                             |
| create_gc_cycles          | 1.43 ms                                                | 1.55 ms: 1.08x slower                                                            |
| docutils                  | 2.66 sec                                               | 2.87 sec: 1.08x slower                                                           |
| pickle                    | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| aiohttp                   | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                            |
| gunicorn                  | 1.20 ms                                                | 1.31 ms: 1.09x slower                                                            |
| regex_v8                  | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                            |
| html5lib                  | 64.8 ms                                                | 71.1 ms: 1.10x slower                                                            |
| tomli_loads               | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                           |
| xml_etree_process         | 56.9 ms                                                | 62.8 ms: 1.10x slower                                                            |
| sqlglot_optimize          | 55.3 ms                                                | 61.2 ms: 1.11x slower                                                            |
| crypto_pyaes              | 76.7 ms                                                | 85.4 ms: 1.11x slower                                                            |
| unpickle                  | 13.8 us                                                | 15.4 us: 1.11x slower                                                            |
| raytrace                  | 309 ms                                                 | 346 ms: 1.12x slower                                                             |
| pycparser                 | 1.19 sec                                               | 1.33 sec: 1.12x slower                                                           |
| xml_etree_generate        | 81.1 ms                                                | 91.6 ms: 1.13x slower                                                            |
| richards                  | 49.8 ms                                                | 56.3 ms: 1.13x slower                                                            |
| 2to3                      | 264 ms                                                 | 300 ms: 1.14x slower                                                             |
| dulwich_log               | 64.6 ms                                                | 73.7 ms: 1.14x slower                                                            |
| pickle_list               | 4.59 us                                                | 5.25 us: 1.14x slower                                                            |
| sqlite_synth              | 2.57 us                                                | 2.95 us: 1.15x slower                                                            |
| unpickle_pure_python      | 242 us                                                 | 278 us: 1.15x slower                                                             |
| nqueens                   | 87.9 ms                                                | 101 ms: 1.15x slower                                                             |
| pprint_safe_repr          | 747 ms                                                 | 866 ms: 1.16x slower                                                             |
| pprint_pformat            | 1.55 sec                                               | 1.82 sec: 1.17x slower                                                           |
| fannkuch                  | 405 ms                                                 | 480 ms: 1.18x slower                                                             |
| float                     | 78.9 ms                                                | 94.7 ms: 1.20x slower                                                            |
| go                        | 149 ms                                                 | 179 ms: 1.20x slower                                                             |
| mako                      | 10.7 ms                                                | 12.9 ms: 1.21x slower                                                            |
| genshi_xml                | 53.4 ms                                                | 64.9 ms: 1.21x slower                                                            |
| scimark_monte_carlo       | 70.7 ms                                                | 85.9 ms: 1.21x slower                                                            |
| python_startup            | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| scimark_sparse_mat_mult   | 5.03 ms                                                | 6.20 ms: 1.23x slower                                                            |
| coverage                  | 78.8 ms                                                | 97.8 ms: 1.24x slower                                                            |
| genshi_text               | 22.5 ms                                                | 28.0 ms: 1.24x slower                                                            |
| regex_compile             | 141 ms                                                 | 178 ms: 1.26x slower                                                             |
| scimark_sor               | 121 ms                                                 | 154 ms: 1.27x slower                                                             |
| nbody                     | 96.0 ms                                                | 123 ms: 1.28x slower                                                             |
| async_generators          | 374 ms                                                 | 480 ms: 1.29x slower                                                             |
| spectral_norm             | 108 ms                                                 | 140 ms: 1.29x slower                                                             |
| unpack_sequence           | 43.5 ns                                                | 56.1 ns: 1.29x slower                                                            |
| telco                     | 6.86 ms                                                | 8.85 ms: 1.29x slower                                                            |
| scimark_fft               | 345 ms                                                 | 450 ms: 1.30x slower                                                             |
| hexiom                    | 6.89 ms                                                | 9.07 ms: 1.32x slower                                                            |
| mypy2                     | 686 ms                                                 | 918 ms: 1.34x slower                                                             |
| pyflate                   | 434 ms                                                 | 593 ms: 1.37x slower                                                             |
| scimark_lu                | 116 ms                                                 | 160 ms: 1.38x slower                                                             |
| python_startup_no_site    | 6.01 ms                                                | 9.07 ms: 1.51x slower                                                            |
| Geometric mean            | (ref)                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, deepcopy
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.01x
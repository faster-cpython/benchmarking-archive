# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 0bbd7af
- commit date: 2024-04-08
- overall geometric mean: 1.05x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 269 ms: 1.02x faster                                                             |
| chameleon      | 7.41 ms                                                | 6.83 ms: 1.09x faster                                                            |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| tornado_http   | 103 ms                                                 | 94.5 ms: 1.09x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 922 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 606 ms: 1.20x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 87.9 ms: 1.10x faster                                                            |
| float          | 84.7 ms                                                | 77.6 ms: 1.09x faster                                                            |
| pidigits       | 187 ms                                                 | 197 ms: 1.05x slower                                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.66 ms: 1.01x slower                                                            |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8       | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.12 sec: 1.10x faster                                                           |
| pickle_pure_python   | 324 us                                                 | 298 us: 1.09x faster                                                             |
| unpickle_list        | 5.29 us                                                | 5.01 us: 1.06x faster                                                            |
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                            |
| unpickle_pure_python | 230 us                                                 | 220 us: 1.05x faster                                                             |
| xml_etree_process    | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                            |
| json_loads           | 28.5 us                                                | 28.8 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| pickle_list          | 5.08 us                                                | 5.19 us: 1.02x slower                                                            |
| pickle_dict          | 35.5 us                                                | 36.4 us: 1.02x slower                                                            |
| pickle               | 11.6 us                                                | 12.1 us: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 8.95 ms: 1.29x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 112 us: 1.41x faster                                                             |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.7 us: 1.30x faster                                                            |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 922 ms: 1.25x faster                                                             |
| raytrace                   | 312 ms                                                 | 259 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 606 ms: 1.20x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.19 ms: 1.17x faster                                                            |
| logging_format             | 7.23 us                                                | 6.31 us: 1.15x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.66 us: 1.14x faster                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 66.4 ms: 1.13x faster                                                            |
| mypy2                      | 830 ms                                                 | 740 ms: 1.12x faster                                                             |
| chaos                      | 67.0 ms                                                | 59.9 ms: 1.12x faster                                                            |
| deepcopy_memo              | 40.7 us                                                | 36.4 us: 1.12x faster                                                            |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                            |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                             |
| nbody                      | 97.0 ms                                                | 87.9 ms: 1.10x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.12 sec: 1.10x faster                                                           |
| crypto_pyaes               | 81.9 ms                                                | 74.6 ms: 1.10x faster                                                            |
| float                      | 84.7 ms                                                | 77.6 ms: 1.09x faster                                                            |
| fannkuch                   | 417 ms                                                 | 383 ms: 1.09x faster                                                             |
| tornado_http               | 103 ms                                                 | 94.5 ms: 1.09x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 298 us: 1.09x faster                                                             |
| chameleon                  | 7.41 ms                                                | 6.83 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                             |
| sympy_str                  | 300 ms                                                 | 278 ms: 1.08x faster                                                             |
| deepcopy                   | 371 us                                                 | 350 us: 1.06x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.16 us: 1.06x faster                                                            |
| pprint_safe_repr           | 776 ms                                                 | 732 ms: 1.06x faster                                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.06x faster                                                            |
| spectral_norm              | 115 ms                                                 | 109 ms: 1.06x faster                                                             |
| unpickle_list              | 5.29 us                                                | 5.01 us: 1.06x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                                            |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 220 us: 1.05x faster                                                             |
| coroutines                 | 23.2 ms                                                | 22.1 ms: 1.05x faster                                                            |
| pprint_pformat             | 1.57 sec                                               | 1.50 sec: 1.05x faster                                                           |
| scimark_sor                | 129 ms                                                 | 124 ms: 1.05x faster                                                             |
| async_generators           | 463 ms                                                 | 443 ms: 1.04x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.5 ms: 1.04x faster                                                            |
| logging_silent             | 104 ns                                                 | 101 ns: 1.04x faster                                                             |
| nqueens                    | 83.3 ms                                                | 80.6 ms: 1.03x faster                                                            |
| pyflate                    | 482 ms                                                 | 467 ms: 1.03x faster                                                             |
| scimark_fft                | 382 ms                                                 | 371 ms: 1.03x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.23 ms: 1.03x faster                                                            |
| scimark_lu                 | 118 ms                                                 | 115 ms: 1.02x faster                                                             |
| sympy_expand               | 478 ms                                                 | 468 ms: 1.02x faster                                                             |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                                           |
| dulwich_log                | 68.5 ms                                                | 67.3 ms: 1.02x faster                                                            |
| 2to3                       | 274 ms                                                 | 269 ms: 1.02x faster                                                             |
| mdp                        | 2.63 sec                                               | 2.59 sec: 1.02x faster                                                           |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                             |
| xml_etree_process          | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                            |
| xml_etree_generate         | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                            |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                             |
| gc_traversal               | 3.79 ms                                                | 3.75 ms: 1.01x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 834 us: 1.01x faster                                                             |
| sqlglot_normalize          | 110 ms                                                 | 111 ms: 1.00x slower                                                             |
| sqlglot_optimize           | 54.8 ms                                                | 55.3 ms: 1.01x slower                                                            |
| json_loads                 | 28.5 us                                                | 28.8 us: 1.01x slower                                                            |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.66 ms: 1.01x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| pickle_list                | 5.08 us                                                | 5.19 us: 1.02x slower                                                            |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                            |
| pickle_dict                | 35.5 us                                                | 36.4 us: 1.02x slower                                                            |
| richards                   | 45.8 ms                                                | 47.1 ms: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                                             |
| asyncio_tcp                | 491 ms                                                 | 505 ms: 1.03x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 2.92 us: 1.03x slower                                                            |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| richards_super             | 51.5 ms                                                | 53.1 ms: 1.03x slower                                                            |
| json                       | 5.26 ms                                                | 5.43 ms: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.22 ms: 1.03x slower                                                            |
| pickle                     | 11.6 us                                                | 12.1 us: 1.04x slower                                                            |
| pidigits                   | 187 ms                                                 | 197 ms: 1.05x slower                                                             |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8                   | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.72 ms: 1.17x slower                                                            |
| telco                      | 7.10 ms                                                | 8.80 ms: 1.24x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 8.95 ms: 1.29x slower                                                            |
| coverage                   | 72.7 ms                                                | 96.3 ms: 1.33x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                                     |

Benchmark hidden because not significant (3): bench_mp_pool, xml_etree_iterparse, xml_etree_parse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-0bbd7af/bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x
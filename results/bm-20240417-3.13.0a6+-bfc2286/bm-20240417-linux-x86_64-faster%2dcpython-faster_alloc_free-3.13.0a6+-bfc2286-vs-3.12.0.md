# Results vs. 3.12.0

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: bfc2286
- commit date: 2024-04-17
- overall geometric mean: 1.04x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 272 ms: 1.01x faster                                                          |
| chameleon      | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                         |
| docutils       | 2.77 sec                                               | 2.84 sec: 1.03x slower                                                        |
| tornado_http   | 103 ms                                                 | 94.6 ms: 1.08x faster                                                         |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                          |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.30x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 924 ms: 1.28x faster                                                          |
| async_tree_io              | 1.16 sec                                               | 912 ms: 1.27x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 598 ms: 1.21x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 602 ms: 1.21x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 84.7 ms: 1.15x faster                                                         |
| float          | 84.7 ms                                                | 77.6 ms: 1.09x faster                                                         |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                  | 1.07x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 136 ms: 1.09x faster                                                          |
| regex_effbot   | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                         |
| regex_dna      | 212 ms                                                 | 224 ms: 1.06x slower                                                          |
| regex_v8       | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                         |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                                          |
| tomli_loads          | 2.33 sec                                               | 2.24 sec: 1.04x faster                                                        |
| unpickle_pure_python | 230 us                                                 | 222 us: 1.04x faster                                                          |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                         |
| unpickle             | 15.9 us                                                | 15.5 us: 1.02x faster                                                         |
| xml_etree_process    | 61.7 ms                                                | 60.8 ms: 1.01x faster                                                         |
| unpickle_list        | 5.29 us                                                | 5.24 us: 1.01x faster                                                         |
| xml_etree_generate   | 89.2 ms                                                | 88.3 ms: 1.01x faster                                                         |
| pickle_dict          | 35.5 us                                                | 36.0 us: 1.01x slower                                                         |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                         |
| pickle               | 11.6 us                                                | 12.1 us: 1.04x slower                                                         |
| pickle_list          | 5.08 us                                                | 5.41 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.07 ms: 1.02x slower                                                         |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.1 ms: 1.07x faster                                                         |
| django_template | 34.6 ms                                                | 35.1 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 115 us: 1.37x faster                                                          |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                          |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.30x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 924 ms: 1.28x faster                                                          |
| comprehensions             | 21.8 us                                                | 17.0 us: 1.28x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 912 ms: 1.27x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 598 ms: 1.21x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 602 ms: 1.21x faster                                                          |
| raytrace                   | 312 ms                                                 | 265 ms: 1.18x faster                                                          |
| deltablue                  | 3.72 ms                                                | 3.23 ms: 1.15x faster                                                         |
| nbody                      | 97.0 ms                                                | 84.7 ms: 1.15x faster                                                         |
| mypy2                      | 830 ms                                                 | 739 ms: 1.12x faster                                                          |
| logging_format             | 7.23 us                                                | 6.47 us: 1.12x faster                                                         |
| pathlib                    | 19.3 ms                                                | 17.4 ms: 1.11x faster                                                         |
| logging_simple             | 6.46 us                                                | 5.81 us: 1.11x faster                                                         |
| chaos                      | 67.0 ms                                                | 60.4 ms: 1.11x faster                                                         |
| crypto_pyaes               | 81.9 ms                                                | 74.6 ms: 1.10x faster                                                         |
| float                      | 84.7 ms                                                | 77.6 ms: 1.09x faster                                                         |
| scimark_monte_carlo        | 75.1 ms                                                | 68.9 ms: 1.09x faster                                                         |
| regex_compile              | 148 ms                                                 | 136 ms: 1.09x faster                                                          |
| tornado_http               | 103 ms                                                 | 94.6 ms: 1.08x faster                                                         |
| mako                       | 11.9 ms                                                | 11.1 ms: 1.07x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.07x faster                                                          |
| deepcopy_memo              | 40.7 us                                                | 38.3 us: 1.06x faster                                                         |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                                          |
| generators                 | 31.2 ms                                                | 29.5 ms: 1.06x faster                                                         |
| sympy_str                  | 300 ms                                                 | 283 ms: 1.06x faster                                                          |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.05x faster                                                         |
| sympy_integrate            | 21.4 ms                                                | 20.5 ms: 1.04x faster                                                         |
| chameleon                  | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                         |
| deepcopy                   | 371 us                                                 | 357 us: 1.04x faster                                                          |
| fannkuch                   | 417 ms                                                 | 401 ms: 1.04x faster                                                          |
| async_generators           | 463 ms                                                 | 446 ms: 1.04x faster                                                          |
| tomli_loads                | 2.33 sec                                               | 2.24 sec: 1.04x faster                                                        |
| unpickle_pure_python       | 230 us                                                 | 222 us: 1.04x faster                                                          |
| scimark_sor                | 129 ms                                                 | 125 ms: 1.03x faster                                                          |
| deepcopy_reduce            | 3.35 us                                                | 3.24 us: 1.03x faster                                                         |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                         |
| pprint_safe_repr           | 776 ms                                                 | 752 ms: 1.03x faster                                                          |
| scimark_lu                 | 118 ms                                                 | 115 ms: 1.03x faster                                                          |
| nqueens                    | 83.3 ms                                                | 81.0 ms: 1.03x faster                                                         |
| dulwich_log                | 68.5 ms                                                | 66.7 ms: 1.03x faster                                                         |
| unpickle                   | 15.9 us                                                | 15.5 us: 1.02x faster                                                         |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                                        |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                         |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.02x faster                                                          |
| scimark_fft                | 382 ms                                                 | 376 ms: 1.02x faster                                                          |
| xml_etree_process          | 61.7 ms                                                | 60.8 ms: 1.01x faster                                                         |
| unpickle_list              | 5.29 us                                                | 5.24 us: 1.01x faster                                                         |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| xml_etree_generate         | 89.2 ms                                                | 88.3 ms: 1.01x faster                                                         |
| 2to3                       | 274 ms                                                 | 272 ms: 1.01x faster                                                          |
| gc_traversal               | 3.79 ms                                                | 3.76 ms: 1.01x faster                                                         |
| sympy_expand               | 478 ms                                                 | 476 ms: 1.01x faster                                                          |
| hexiom                     | 6.41 ms                                                | 6.38 ms: 1.00x faster                                                         |
| bench_thread_pool          | 842 us                                                 | 840 us: 1.00x faster                                                          |
| sqlglot_normalize          | 110 ms                                                 | 111 ms: 1.01x slower                                                          |
| logging_silent             | 104 ns                                                 | 105 ns: 1.01x slower                                                          |
| sqlglot_optimize           | 54.8 ms                                                | 55.5 ms: 1.01x slower                                                         |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                          |
| pickle_dict                | 35.5 us                                                | 36.0 us: 1.01x slower                                                         |
| django_template            | 34.6 ms                                                | 35.1 ms: 1.01x slower                                                         |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                         |
| python_startup_no_site     | 6.94 ms                                                | 7.07 ms: 1.02x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                         |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                         |
| docutils                   | 2.77 sec                                               | 2.84 sec: 1.03x slower                                                        |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.21 ms: 1.03x slower                                                         |
| regex_effbot               | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                         |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                          |
| asyncio_websockets         | 551 ms                                                 | 569 ms: 1.03x slower                                                          |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.03x slower                                                        |
| sqlite_synth               | 2.83 us                                                | 2.93 us: 1.03x slower                                                         |
| asyncio_tcp                | 491 ms                                                 | 508 ms: 1.04x slower                                                          |
| pickle                     | 11.6 us                                                | 12.1 us: 1.04x slower                                                         |
| richards_super             | 51.5 ms                                                | 54.0 ms: 1.05x slower                                                         |
| richards                   | 45.8 ms                                                | 48.0 ms: 1.05x slower                                                         |
| regex_dna                  | 212 ms                                                 | 224 ms: 1.06x slower                                                          |
| spectral_norm              | 115 ms                                                 | 122 ms: 1.06x slower                                                          |
| mdp                        | 2.63 sec                                               | 2.80 sec: 1.06x slower                                                        |
| pickle_list                | 5.08 us                                                | 5.41 us: 1.06x slower                                                         |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                         |
| regex_v8                   | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                         |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                         |
| telco                      | 7.10 ms                                                | 8.60 ms: 1.21x slower                                                         |
| coverage                   | 72.7 ms                                                | 97.7 ms: 1.34x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                  |

Benchmark hidden because not significant (6): pycparser, json, dask, xml_etree_parse, pyflate, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240417-3.13.0a6+-bfc2286/bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x
# Results vs. 3.12.0

- fork: faster-cpython
- ref: call_cmethod
- machine: linux-x86_64
- commit hash: 5c20c52
- commit date: 2024-04-10
- overall geometric mean: 1.04x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 271 ms: 1.01x faster                                                     |
| chameleon      | 7.41 ms                                                | 7.03 ms: 1.05x faster                                                    |
| docutils       | 2.77 sec                                               | 2.84 sec: 1.03x slower                                                   |
| tornado_http   | 103 ms                                                 | 94.8 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 346 ms: 1.36x faster                                                     |
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.34x faster                                                     |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 920 ms: 1.29x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 601 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 606 ms: 1.20x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 88.5 ms: 1.10x faster                                                    |
| float          | 84.7 ms                                                | 78.7 ms: 1.08x faster                                                    |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                     |
| regex_effbot   | 3.61 ms                                                | 3.70 ms: 1.03x slower                                                    |
| regex_dna      | 212 ms                                                 | 218 ms: 1.03x slower                                                     |
| regex_v8       | 23.1 ms                                                | 24.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.00x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.15 sec: 1.08x faster                                                   |
| pickle_pure_python   | 324 us                                                 | 302 us: 1.07x faster                                                     |
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                    |
| unpickle_pure_python | 230 us                                                 | 222 us: 1.04x faster                                                     |
| pickle_dict          | 35.5 us                                                | 34.9 us: 1.02x faster                                                    |
| xml_etree_process    | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                    |
| xml_etree_generate   | 89.2 ms                                                | 88.3 ms: 1.01x faster                                                    |
| unpickle_list        | 5.29 us                                                | 5.25 us: 1.01x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (5): pickle_list, json_loads, xml_etree_iterparse, pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                    |
| python_startup_no_site | 6.94 ms                                                | 8.95 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|-----------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 346 ms: 1.36x faster                                                     |
| typing_runtime_protocols   | 158 us                                                 | 117 us: 1.35x faster                                                     |
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.34x faster                                                     |
| comprehensions             | 21.8 us                                                | 16.6 us: 1.31x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 920 ms: 1.29x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 601 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 606 ms: 1.20x faster                                                     |
| raytrace                   | 312 ms                                                 | 262 ms: 1.19x faster                                                     |
| deltablue                  | 3.72 ms                                                | 3.19 ms: 1.17x faster                                                    |
| logging_format             | 7.23 us                                                | 6.39 us: 1.13x faster                                                    |
| mypy2                      | 830 ms                                                 | 738 ms: 1.12x faster                                                     |
| scimark_monte_carlo        | 75.1 ms                                                | 67.4 ms: 1.11x faster                                                    |
| logging_simple             | 6.46 us                                                | 5.85 us: 1.10x faster                                                    |
| chaos                      | 67.0 ms                                                | 60.6 ms: 1.10x faster                                                    |
| mako                       | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                    |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                     |
| nbody                      | 97.0 ms                                                | 88.5 ms: 1.10x faster                                                    |
| tomli_loads                | 2.33 sec                                               | 2.15 sec: 1.08x faster                                                   |
| tornado_http               | 103 ms                                                 | 94.8 ms: 1.08x faster                                                    |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                     |
| float                      | 84.7 ms                                                | 78.7 ms: 1.08x faster                                                    |
| pickle_pure_python         | 324 us                                                 | 302 us: 1.07x faster                                                     |
| sympy_str                  | 300 ms                                                 | 279 ms: 1.07x faster                                                     |
| fannkuch                   | 417 ms                                                 | 389 ms: 1.07x faster                                                     |
| crypto_pyaes               | 81.9 ms                                                | 76.6 ms: 1.07x faster                                                    |
| scimark_fft                | 382 ms                                                 | 360 ms: 1.06x faster                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.06x faster                                                    |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                    |
| deepcopy_memo              | 40.7 us                                                | 38.5 us: 1.06x faster                                                    |
| chameleon                  | 7.41 ms                                                | 7.03 ms: 1.05x faster                                                    |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                    |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                | 3.19 us: 1.05x faster                                                    |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                                    |
| scimark_lu                 | 118 ms                                                 | 113 ms: 1.05x faster                                                     |
| scimark_sor                | 129 ms                                                 | 123 ms: 1.05x faster                                                     |
| async_generators           | 463 ms                                                 | 445 ms: 1.04x faster                                                     |
| hexiom                     | 6.41 ms                                                | 6.18 ms: 1.04x faster                                                    |
| pprint_safe_repr           | 776 ms                                                 | 749 ms: 1.04x faster                                                     |
| logging_silent             | 104 ns                                                 | 101 ns: 1.04x faster                                                     |
| unpickle_pure_python       | 230 us                                                 | 222 us: 1.04x faster                                                     |
| deepcopy                   | 371 us                                                 | 359 us: 1.03x faster                                                     |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                    |
| nqueens                    | 83.3 ms                                                | 80.9 ms: 1.03x faster                                                    |
| pycparser                  | 1.18 sec                                               | 1.15 sec: 1.03x faster                                                   |
| dulwich_log                | 68.5 ms                                                | 66.9 ms: 1.02x faster                                                    |
| pprint_pformat             | 1.57 sec                                               | 1.53 sec: 1.02x faster                                                   |
| pathlib                    | 19.3 ms                                                | 19.0 ms: 1.02x faster                                                    |
| pickle_dict                | 35.5 us                                                | 34.9 us: 1.02x faster                                                    |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.02x faster                                                     |
| 2to3                       | 274 ms                                                 | 271 ms: 1.01x faster                                                     |
| pyflate                    | 482 ms                                                 | 476 ms: 1.01x faster                                                     |
| sympy_expand               | 478 ms                                                 | 473 ms: 1.01x faster                                                     |
| bench_thread_pool          | 842 us                                                 | 833 us: 1.01x faster                                                     |
| xml_etree_process          | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                    |
| xml_etree_generate         | 89.2 ms                                                | 88.3 ms: 1.01x faster                                                    |
| unpickle_list              | 5.29 us                                                | 5.25 us: 1.01x faster                                                    |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                    |
| sqlglot_optimize           | 54.8 ms                                                | 55.2 ms: 1.01x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                    |
| spectral_norm              | 115 ms                                                 | 116 ms: 1.01x slower                                                     |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                     |
| asyncio_tcp                | 491 ms                                                 | 498 ms: 1.01x slower                                                     |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                    |
| json                       | 5.26 ms                                                | 5.36 ms: 1.02x slower                                                    |
| richards                   | 45.8 ms                                                | 47.0 ms: 1.02x slower                                                    |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.03x slower                                                    |
| regex_effbot               | 3.61 ms                                                | 3.70 ms: 1.03x slower                                                    |
| richards_super             | 51.5 ms                                                | 52.9 ms: 1.03x slower                                                    |
| docutils                   | 2.77 sec                                               | 2.84 sec: 1.03x slower                                                   |
| regex_dna                  | 212 ms                                                 | 218 ms: 1.03x slower                                                     |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                     |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                   |
| sqlite_synth               | 2.83 us                                                | 2.93 us: 1.03x slower                                                    |
| regex_v8                   | 23.1 ms                                                | 24.2 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.30 ms: 1.05x slower                                                    |
| mdp                        | 2.63 sec                                               | 2.77 sec: 1.05x slower                                                   |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                    |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                    |
| telco                      | 7.10 ms                                                | 8.70 ms: 1.23x slower                                                    |
| python_startup_no_site     | 6.94 ms                                                | 8.95 ms: 1.29x slower                                                    |
| coverage                   | 72.7 ms                                                | 96.8 ms: 1.33x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (9): dask, pickle_list, json_loads, xml_etree_iterparse, gc_traversal, go, pickle, sqlglot_normalize, xml_etree_parse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-5c20c52/bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x
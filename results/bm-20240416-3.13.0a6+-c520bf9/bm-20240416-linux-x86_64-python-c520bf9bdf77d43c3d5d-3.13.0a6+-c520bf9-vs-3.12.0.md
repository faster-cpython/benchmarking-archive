# Results vs. 3.12.0

- fork: python
- ref: c520bf9bdf77d43c3d5d
- machine: linux-x86_64
- commit hash: c520bf9
- commit date: 2024-04-16
- overall geometric mean: 1.04x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 270 ms: 1.01x faster                                                   |
| chameleon      | 7.41 ms                                                | 6.94 ms: 1.07x faster                                                  |
| docutils       | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                 |
| tornado_http   | 103 ms                                                 | 93.9 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 935 ms: 1.26x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 464 ms: 1.25x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 936 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 607 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 90.0 ms: 1.08x faster                                                  |
| float          | 84.7 ms                                                | 78.7 ms: 1.08x faster                                                  |
| pidigits       | 187 ms                                                 | 206 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 136 ms: 1.09x faster                                                   |
| regex_dna      | 212 ms                                                 | 218 ms: 1.03x slower                                                   |
| regex_effbot   | 3.61 ms                                                | 3.74 ms: 1.04x slower                                                  |
| regex_v8       | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 299 us: 1.08x faster                                                   |
| tomli_loads          | 2.33 sec                                               | 2.17 sec: 1.07x faster                                                 |
| unpickle_list        | 5.29 us                                                | 4.99 us: 1.06x faster                                                  |
| unpickle_pure_python | 230 us                                                 | 217 us: 1.06x faster                                                   |
| unpickle             | 15.9 us                                                | 15.2 us: 1.04x faster                                                  |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                  |
| xml_etree_process    | 61.7 ms                                                | 60.8 ms: 1.02x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 88.8 ms: 1.00x faster                                                  |
| xml_etree_iterparse  | 107 ms                                                 | 107 ms: 1.01x slower                                                   |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                  |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                  |
| pickle_list          | 5.08 us                                                | 5.33 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.1 ms: 1.07x faster                                                  |
| django_template | 34.6 ms                                                | 35.8 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 115 us: 1.37x faster                                                   |
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                                   |
| comprehensions             | 21.8 us                                                | 16.9 us: 1.29x faster                                                  |
| async_tree_io_tg           | 1.18 sec                                               | 935 ms: 1.26x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 464 ms: 1.25x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 936 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 607 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                                   |
| raytrace                   | 312 ms                                                 | 264 ms: 1.18x faster                                                   |
| deltablue                  | 3.72 ms                                                | 3.26 ms: 1.14x faster                                                  |
| logging_format             | 7.23 us                                                | 6.40 us: 1.13x faster                                                  |
| mypy2                      | 830 ms                                                 | 737 ms: 1.13x faster                                                   |
| logging_simple             | 6.46 us                                                | 5.80 us: 1.11x faster                                                  |
| chaos                      | 67.0 ms                                                | 60.2 ms: 1.11x faster                                                  |
| pathlib                    | 19.3 ms                                                | 17.5 ms: 1.11x faster                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 68.4 ms: 1.10x faster                                                  |
| regex_compile              | 148 ms                                                 | 136 ms: 1.09x faster                                                   |
| tornado_http               | 103 ms                                                 | 93.9 ms: 1.09x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 299 us: 1.08x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 37.7 us: 1.08x faster                                                  |
| nbody                      | 97.0 ms                                                | 90.0 ms: 1.08x faster                                                  |
| float                      | 84.7 ms                                                | 78.7 ms: 1.08x faster                                                  |
| mako                       | 11.9 ms                                                | 11.1 ms: 1.07x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 76.3 ms: 1.07x faster                                                  |
| tomli_loads                | 2.33 sec                                               | 2.17 sec: 1.07x faster                                                 |
| chameleon                  | 7.41 ms                                                | 6.94 ms: 1.07x faster                                                  |
| fannkuch                   | 417 ms                                                 | 391 ms: 1.07x faster                                                   |
| sympy_str                  | 300 ms                                                 | 282 ms: 1.06x faster                                                   |
| unpickle_list              | 5.29 us                                                | 4.99 us: 1.06x faster                                                  |
| unpickle_pure_python       | 230 us                                                 | 217 us: 1.06x faster                                                   |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                  |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.05x faster                                                  |
| scimark_sor                | 129 ms                                                 | 123 ms: 1.05x faster                                                   |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.04x faster                                                  |
| deepcopy                   | 371 us                                                 | 356 us: 1.04x faster                                                   |
| async_generators           | 463 ms                                                 | 445 ms: 1.04x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.03x faster                                                  |
| scimark_fft                | 382 ms                                                 | 369 ms: 1.03x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                  |
| dulwich_log                | 68.5 ms                                                | 66.4 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 776 ms                                                 | 754 ms: 1.03x faster                                                   |
| pycparser                  | 1.18 sec                                               | 1.15 sec: 1.03x faster                                                 |
| pyflate                    | 482 ms                                                 | 471 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.53 sec: 1.02x faster                                                 |
| json                       | 5.26 ms                                                | 5.15 ms: 1.02x faster                                                  |
| nqueens                    | 83.3 ms                                                | 81.7 ms: 1.02x faster                                                  |
| spectral_norm              | 115 ms                                                 | 113 ms: 1.02x faster                                                   |
| coroutines                 | 23.2 ms                                                | 22.7 ms: 1.02x faster                                                  |
| xml_etree_process          | 61.7 ms                                                | 60.8 ms: 1.02x faster                                                  |
| 2to3                       | 274 ms                                                 | 270 ms: 1.01x faster                                                   |
| scimark_lu                 | 118 ms                                                 | 117 ms: 1.01x faster                                                   |
| mdp                        | 2.63 sec                                               | 2.60 sec: 1.01x faster                                                 |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                   |
| generators                 | 31.2 ms                                                | 30.9 ms: 1.01x faster                                                  |
| sympy_expand               | 478 ms                                                 | 475 ms: 1.01x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| xml_etree_generate         | 89.2 ms                                                | 88.8 ms: 1.00x faster                                                  |
| hexiom                     | 6.41 ms                                                | 6.43 ms: 1.00x slower                                                  |
| xml_etree_iterparse        | 107 ms                                                 | 107 ms: 1.01x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                  |
| sqlglot_optimize           | 54.8 ms                                                | 55.6 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 110 ms                                                 | 112 ms: 1.01x slower                                                   |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                  |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                  |
| gc_traversal               | 3.79 ms                                                | 3.87 ms: 1.02x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                   |
| docutils                   | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                 |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                  |
| python_startup_no_site     | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.20 ms: 1.03x slower                                                  |
| regex_dna                  | 212 ms                                                 | 218 ms: 1.03x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.03x slower                                                 |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 507 ms: 1.03x slower                                                   |
| django_template            | 34.6 ms                                                | 35.8 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 2.93 us: 1.04x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.74 ms: 1.04x slower                                                  |
| richards_super             | 51.5 ms                                                | 53.7 ms: 1.04x slower                                                  |
| richards                   | 45.8 ms                                                | 47.9 ms: 1.04x slower                                                  |
| pickle_list                | 5.08 us                                                | 5.33 us: 1.05x slower                                                  |
| regex_v8                   | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                  |
| pidigits                   | 187 ms                                                 | 206 ms: 1.10x slower                                                   |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                                  |
| telco                      | 7.10 ms                                                | 8.55 ms: 1.20x slower                                                  |
| coverage                   | 72.7 ms                                                | 98.6 ms: 1.36x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (5): logging_silent, pickle_dict, dask, bench_thread_pool, xml_etree_parse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240416-3.13.0a6+-c520bf9/bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x
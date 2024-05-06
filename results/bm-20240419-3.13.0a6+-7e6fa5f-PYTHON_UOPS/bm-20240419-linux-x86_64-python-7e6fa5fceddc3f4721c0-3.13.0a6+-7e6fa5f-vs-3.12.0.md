# Results vs. 3.12.0

- fork: python
- ref: 7e6fa5fceddc3f4721c0
- machine: linux-x86_64
- commit hash: 7e6fa5f
- commit date: 2024-04-19
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 301 ms: 1.10x slower                                                   |
| chameleon      | 7.41 ms                                                | 7.58 ms: 1.02x slower                                                  |
| docutils       | 2.77 sec                                               | 3.08 sec: 1.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 352 ms: 1.28x faster                                                   |
| async_tree_none            | 472 ms                                                 | 379 ms: 1.25x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 463 ms: 1.24x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 980 ms: 1.21x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 979 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 624 ms: 1.16x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 506 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 637 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 191 ms: 1.02x slower                                                   |
| float          | 84.7 ms                                                | 89.3 ms: 1.05x slower                                                  |
| nbody          | 97.0 ms                                                | 121 ms: 1.25x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.54 ms: 1.02x faster                                                  |
| regex_dna      | 212 ms                                                 | 222 ms: 1.05x slower                                                   |
| regex_v8       | 23.1 ms                                                | 25.2 ms: 1.09x slower                                                  |
| regex_compile  | 148 ms                                                 | 179 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| json_loads           | 28.5 us                                                | 27.3 us: 1.05x faster                                                  |
| unpickle_list        | 5.29 us                                                | 5.10 us: 1.04x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 316 us: 1.02x faster                                                   |
| unpickle             | 15.9 us                                                | 15.5 us: 1.02x faster                                                  |
| pickle_dict          | 35.5 us                                                | 36.1 us: 1.02x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| xml_etree_process    | 61.7 ms                                                | 63.9 ms: 1.03x slower                                                  |
| xml_etree_generate   | 89.2 ms                                                | 93.0 ms: 1.04x slower                                                  |
| xml_etree_iterparse  | 107 ms                                                 | 112 ms: 1.05x slower                                                   |
| pickle               | 11.6 us                                                | 12.2 us: 1.05x slower                                                  |
| pickle_list          | 5.08 us                                                | 5.37 us: 1.06x slower                                                  |
| tomli_loads          | 2.33 sec                                               | 2.55 sec: 1.10x slower                                                 |
| unpickle_pure_python | 230 us                                                 | 286 us: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.5 ms: 1.14x slower                                                  |
| django_template | 34.6 ms                                                | 40.8 ms: 1.18x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.16x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 119 us: 1.33x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 352 ms: 1.28x faster                                                   |
| async_tree_none            | 472 ms                                                 | 379 ms: 1.25x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 463 ms: 1.24x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 980 ms: 1.21x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 979 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 624 ms: 1.16x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 506 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 637 ms: 1.14x faster                                                   |
| pathlib                    | 19.3 ms                                                | 18.2 ms: 1.06x faster                                                  |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.3 us: 1.05x faster                                                  |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                                  |
| unpickle_list              | 5.29 us                                                | 5.10 us: 1.04x faster                                                  |
| json                       | 5.26 ms                                                | 5.12 ms: 1.03x faster                                                  |
| logging_format             | 7.23 us                                                | 7.05 us: 1.03x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 316 us: 1.02x faster                                                   |
| unpickle                   | 15.9 us                                                | 15.5 us: 1.02x faster                                                  |
| regex_effbot               | 3.61 ms                                                | 3.54 ms: 1.02x faster                                                  |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                  |
| gc_traversal               | 3.79 ms                                                | 3.76 ms: 1.01x faster                                                  |
| logging_simple             | 6.46 us                                                | 6.41 us: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| async_generators           | 463 ms                                                 | 468 ms: 1.01x slower                                                   |
| pickle_dict                | 35.5 us                                                | 36.1 us: 1.02x slower                                                  |
| logging_silent             | 104 ns                                                 | 107 ns: 1.02x slower                                                   |
| pidigits                   | 187 ms                                                 | 191 ms: 1.02x slower                                                   |
| chameleon                  | 7.41 ms                                                | 7.58 ms: 1.02x slower                                                  |
| deepcopy                   | 371 us                                                 | 380 us: 1.02x slower                                                   |
| dask                       | 372 ms                                                 | 381 ms: 1.03x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| raytrace                   | 312 ms                                                 | 322 ms: 1.03x slower                                                   |
| xml_etree_process          | 61.7 ms                                                | 63.9 ms: 1.03x slower                                                  |
| xml_etree_generate         | 89.2 ms                                                | 93.0 ms: 1.04x slower                                                  |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 177 ms: 1.05x slower                                                   |
| regex_dna                  | 212 ms                                                 | 222 ms: 1.05x slower                                                   |
| xml_etree_iterparse        | 107 ms                                                 | 112 ms: 1.05x slower                                                   |
| pickle                     | 11.6 us                                                | 12.2 us: 1.05x slower                                                  |
| bench_thread_pool          | 842 us                                                 | 884 us: 1.05x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 516 ms: 1.05x slower                                                   |
| float                      | 84.7 ms                                                | 89.3 ms: 1.05x slower                                                  |
| pickle_list                | 5.08 us                                                | 5.37 us: 1.06x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.32 ms: 1.06x slower                                                  |
| meteor_contest             | 112 ms                                                 | 120 ms: 1.07x slower                                                   |
| dulwich_log                | 68.5 ms                                                | 73.4 ms: 1.07x slower                                                  |
| sympy_str                  | 300 ms                                                 | 322 ms: 1.07x slower                                                   |
| aiohttp                    | 1.15 ms                                                | 1.24 ms: 1.07x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 3.05 us: 1.08x slower                                                  |
| comprehensions             | 21.8 us                                                | 23.5 us: 1.08x slower                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.82 ms: 1.08x slower                                                  |
| pycparser                  | 1.18 sec                                               | 1.28 sec: 1.08x slower                                                 |
| sympy_integrate            | 21.4 ms                                                | 23.2 ms: 1.08x slower                                                  |
| regex_v8                   | 23.1 ms                                                | 25.2 ms: 1.09x slower                                                  |
| tomli_loads                | 2.33 sec                                               | 2.55 sec: 1.10x slower                                                 |
| 2to3                       | 274 ms                                                 | 301 ms: 1.10x slower                                                   |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.50 ms: 1.10x slower                                                  |
| deltablue                  | 3.72 ms                                                | 4.10 ms: 1.10x slower                                                  |
| docutils                   | 2.77 sec                                               | 3.08 sec: 1.11x slower                                                 |
| sqlglot_normalize          | 110 ms                                                 | 123 ms: 1.11x slower                                                   |
| deepcopy_memo              | 40.7 us                                                | 45.5 us: 1.12x slower                                                  |
| crypto_pyaes               | 81.9 ms                                                | 91.6 ms: 1.12x slower                                                  |
| sympy_expand               | 478 ms                                                 | 536 ms: 1.12x slower                                                   |
| mdp                        | 2.63 sec                                               | 2.99 sec: 1.14x slower                                                 |
| mako                       | 11.9 ms                                                | 13.5 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 54.8 ms                                                | 63.2 ms: 1.15x slower                                                  |
| scimark_fft                | 382 ms                                                 | 445 ms: 1.17x slower                                                   |
| chaos                      | 67.0 ms                                                | 78.5 ms: 1.17x slower                                                  |
| scimark_sor                | 129 ms                                                 | 151 ms: 1.17x slower                                                   |
| django_template            | 34.6 ms                                                | 40.8 ms: 1.18x slower                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 88.8 ms: 1.18x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.98 ms: 1.18x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.20x slower                                                  |
| regex_compile              | 148 ms                                                 | 179 ms: 1.20x slower                                                   |
| fannkuch                   | 417 ms                                                 | 502 ms: 1.20x slower                                                   |
| richards_super             | 51.5 ms                                                | 62.4 ms: 1.21x slower                                                  |
| richards                   | 45.8 ms                                                | 55.9 ms: 1.22x slower                                                  |
| pyflate                    | 482 ms                                                 | 600 ms: 1.24x slower                                                   |
| unpickle_pure_python       | 230 us                                                 | 286 us: 1.24x slower                                                   |
| nbody                      | 97.0 ms                                                | 121 ms: 1.25x slower                                                   |
| pprint_safe_repr           | 776 ms                                                 | 966 ms: 1.25x slower                                                   |
| spectral_norm              | 115 ms                                                 | 144 ms: 1.25x slower                                                   |
| pprint_pformat             | 1.57 sec                                               | 2.01 sec: 1.28x slower                                                 |
| nqueens                    | 83.3 ms                                                | 107 ms: 1.29x slower                                                   |
| telco                      | 7.10 ms                                                | 9.19 ms: 1.29x slower                                                  |
| go                         | 139 ms                                                 | 185 ms: 1.33x slower                                                   |
| coverage                   | 72.7 ms                                                | 98.1 ms: 1.35x slower                                                  |
| scimark_lu                 | 118 ms                                                 | 166 ms: 1.41x slower                                                   |
| hexiom                     | 6.41 ms                                                | 9.55 ms: 1.49x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (3): mypy2, tornado_http, deepcopy_reduce
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240419-3.13.0a6+-7e6fa5f-PYTHON_UOPS/bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.97x
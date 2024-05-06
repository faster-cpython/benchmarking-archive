# Results vs. 3.12.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 752e183
- commit date: 2024-03-31
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.95x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 269 ms: 1.02x faster                                   |
| chameleon      | 7.41 ms                                                | 6.85 ms: 1.08x faster                                  |
| tornado_http   | 103 ms                                                 | 95.0 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 339 ms: 1.33x faster                                   |
| async_tree_memoization     | 578 ms                                                 | 448 ms: 1.29x faster                                   |
| async_tree_io_tg           | 1.18 sec                                               | 921 ms: 1.28x faster                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 448 ms: 1.28x faster                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 579 ms: 1.25x faster                                   |
| async_tree_io              | 1.16 sec                                               | 934 ms: 1.24x faster                                   |
| async_tree_none            | 472 ms                                                 | 386 ms: 1.22x faster                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 596 ms: 1.22x faster                                   |
| Geometric mean             | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.2 ms: 1.10x faster                                  |
| nbody          | 97.0 ms                                                | 89.5 ms: 1.08x faster                                  |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                   |
| regex_effbot   | 3.61 ms                                                | 3.76 ms: 1.04x slower                                  |
| regex_dna      | 212 ms                                                 | 222 ms: 1.05x slower                                   |
| regex_v8       | 23.1 ms                                                | 26.2 ms: 1.13x slower                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 303 us: 1.07x faster                                   |
| pickle_dict          | 35.5 us                                                | 33.6 us: 1.06x faster                                  |
| tomli_loads          | 2.33 sec                                               | 2.22 sec: 1.05x faster                                 |
| unpickle_pure_python | 230 us                                                 | 220 us: 1.05x faster                                   |
| unpickle_list        | 5.29 us                                                | 5.13 us: 1.03x faster                                  |
| xml_etree_process    | 61.7 ms                                                | 59.9 ms: 1.03x faster                                  |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                  |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.03x faster                                  |
| json_loads           | 28.5 us                                                | 28.6 us: 1.00x slower                                  |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                  |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                   |
| xml_etree_parse      | 159 ms                                                 | 163 ms: 1.02x slower                                   |
| unpickle             | 15.9 us                                                | 18.5 us: 1.16x slower                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                  |
| python_startup_no_site | 6.94 ms                                                | 8.99 ms: 1.30x slower                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.9 ms: 1.09x faster                                  |
| django_template | 34.6 ms                                                | 34.2 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 112 us: 1.40x faster                                   |
| async_tree_none_tg         | 450 ms                                                 | 339 ms: 1.33x faster                                   |
| comprehensions             | 21.8 us                                                | 16.4 us: 1.33x faster                                  |
| async_tree_memoization     | 578 ms                                                 | 448 ms: 1.29x faster                                   |
| async_tree_io_tg           | 1.18 sec                                               | 921 ms: 1.28x faster                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 448 ms: 1.28x faster                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 579 ms: 1.25x faster                                   |
| async_tree_io              | 1.16 sec                                               | 934 ms: 1.24x faster                                   |
| async_tree_none            | 472 ms                                                 | 386 ms: 1.22x faster                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 596 ms: 1.22x faster                                   |
| raytrace                   | 312 ms                                                 | 268 ms: 1.17x faster                                   |
| deltablue                  | 3.72 ms                                                | 3.21 ms: 1.16x faster                                  |
| crypto_pyaes               | 81.9 ms                                                | 72.1 ms: 1.13x faster                                  |
| mypy2                      | 830 ms                                                 | 737 ms: 1.13x faster                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 67.6 ms: 1.11x faster                                  |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                   |
| chaos                      | 67.0 ms                                                | 60.4 ms: 1.11x faster                                  |
| logging_format             | 7.23 us                                                | 6.56 us: 1.10x faster                                  |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                   |
| float                      | 84.7 ms                                                | 77.2 ms: 1.10x faster                                  |
| logging_simple             | 6.46 us                                                | 5.90 us: 1.10x faster                                  |
| sympy_str                  | 300 ms                                                 | 274 ms: 1.09x faster                                   |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                  |
| nbody                      | 97.0 ms                                                | 89.5 ms: 1.08x faster                                  |
| chameleon                  | 7.41 ms                                                | 6.85 ms: 1.08x faster                                  |
| tornado_http               | 103 ms                                                 | 95.0 ms: 1.08x faster                                  |
| fannkuch                   | 417 ms                                                 | 387 ms: 1.08x faster                                   |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.71 ms: 1.07x faster                                  |
| pickle_pure_python         | 324 us                                                 | 303 us: 1.07x faster                                   |
| sympy_integrate            | 21.4 ms                                                | 20.0 ms: 1.07x faster                                  |
| deepcopy_memo              | 40.7 us                                                | 38.3 us: 1.06x faster                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.06x faster                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.15 us: 1.06x faster                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                  |
| pickle_dict                | 35.5 us                                                | 33.6 us: 1.06x faster                                  |
| pprint_safe_repr           | 776 ms                                                 | 735 ms: 1.06x faster                                   |
| deepcopy                   | 371 us                                                 | 353 us: 1.05x faster                                   |
| pyflate                    | 482 ms                                                 | 460 ms: 1.05x faster                                   |
| tomli_loads                | 2.33 sec                                               | 2.22 sec: 1.05x faster                                 |
| unpickle_pure_python       | 230 us                                                 | 220 us: 1.05x faster                                   |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                  |
| nqueens                    | 83.3 ms                                                | 79.6 ms: 1.05x faster                                  |
| async_generators           | 463 ms                                                 | 443 ms: 1.05x faster                                   |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                 |
| scimark_sor                | 129 ms                                                 | 124 ms: 1.04x faster                                   |
| logging_silent             | 104 ns                                                 | 100 ns: 1.04x faster                                   |
| meteor_contest             | 112 ms                                                 | 108 ms: 1.04x faster                                   |
| hexiom                     | 6.41 ms                                                | 6.18 ms: 1.04x faster                                  |
| unpickle_list              | 5.29 us                                                | 5.13 us: 1.03x faster                                  |
| xml_etree_process          | 61.7 ms                                                | 59.9 ms: 1.03x faster                                  |
| spectral_norm              | 115 ms                                                 | 112 ms: 1.03x faster                                   |
| sympy_expand               | 478 ms                                                 | 464 ms: 1.03x faster                                   |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                  |
| pickle_list                | 5.08 us                                                | 4.96 us: 1.03x faster                                  |
| 2to3                       | 274 ms                                                 | 269 ms: 1.02x faster                                   |
| pathlib                    | 19.3 ms                                                | 19.0 ms: 1.02x faster                                  |
| bench_thread_pool          | 842 us                                                 | 830 us: 1.01x faster                                   |
| mdp                        | 2.63 sec                                               | 2.60 sec: 1.01x faster                                 |
| dulwich_log                | 68.5 ms                                                | 67.6 ms: 1.01x faster                                  |
| django_template            | 34.6 ms                                                | 34.2 ms: 1.01x faster                                  |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                   |
| scimark_lu                 | 118 ms                                                 | 117 ms: 1.01x faster                                   |
| sqlglot_normalize          | 110 ms                                                 | 110 ms: 1.01x faster                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                  |
| json_loads                 | 28.5 us                                                | 28.6 us: 1.00x slower                                  |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                  |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                   |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                   |
| coroutines                 | 23.2 ms                                                | 23.5 ms: 1.01x slower                                  |
| json                       | 5.26 ms                                                | 5.33 ms: 1.01x slower                                  |
| richards_super             | 51.5 ms                                                | 52.6 ms: 1.02x slower                                  |
| aiohttp                    | 1.15 ms                                                | 1.18 ms: 1.02x slower                                  |
| sqlite_synth               | 2.83 us                                                | 2.90 us: 1.02x slower                                  |
| xml_etree_parse            | 159 ms                                                 | 163 ms: 1.02x slower                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.83 sec: 1.03x slower                                 |
| gunicorn                   | 1.24 ms                                                | 1.28 ms: 1.03x slower                                  |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                   |
| asyncio_websockets         | 551 ms                                                 | 569 ms: 1.03x slower                                   |
| pycparser                  | 1.18 sec                                               | 1.22 sec: 1.03x slower                                 |
| regex_effbot               | 3.61 ms                                                | 3.76 ms: 1.04x slower                                  |
| regex_dna                  | 212 ms                                                 | 222 ms: 1.05x slower                                   |
| gc_traversal               | 3.79 ms                                                | 4.00 ms: 1.05x slower                                  |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                  |
| regex_v8                   | 23.1 ms                                                | 26.2 ms: 1.13x slower                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.67 ms: 1.13x slower                                  |
| unpickle                   | 15.9 us                                                | 18.5 us: 1.16x slower                                  |
| telco                      | 7.10 ms                                                | 8.54 ms: 1.20x slower                                  |
| python_startup_no_site     | 6.94 ms                                                | 8.99 ms: 1.30x slower                                  |
| coverage                   | 72.7 ms                                                | 97.6 ms: 1.34x slower                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (7): scimark_fft, docutils, unpack_sequence, sqlglot_optimize, richards, pickle, go
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240331-3.13.0a5+-752e183/bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.95x
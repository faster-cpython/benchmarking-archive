# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 313 ms: 1.14x slower                                                   |
| chameleon      | 7.41 ms                                                | 7.93 ms: 1.07x slower                                                  |
| docutils       | 2.77 sec                                               | 3.14 sec: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 380 ms: 1.24x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 365 ms: 1.23x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 475 ms: 1.21x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 1.00 sec: 1.18x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 996 ms: 1.16x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 501 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 638 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 639 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 196 ms: 1.05x slower                                                   |
| float          | 84.7 ms                                                | 91.6 ms: 1.08x slower                                                  |
| nbody          | 97.0 ms                                                | 117 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 212 ms                                                 | 219 ms: 1.03x slower                                                   |
| regex_effbot   | 3.61 ms                                                | 3.80 ms: 1.05x slower                                                  |
| regex_v8       | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                  |
| regex_compile  | 148 ms                                                 | 190 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| json_loads           | 28.5 us                                                | 27.5 us: 1.04x faster                                                  |
| unpickle_list        | 5.29 us                                                | 5.12 us: 1.03x faster                                                  |
| pickle_dict          | 35.5 us                                                | 34.5 us: 1.03x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 317 us: 1.02x faster                                                   |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 107 ms                                                 | 110 ms: 1.03x slower                                                   |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| xml_etree_process    | 61.7 ms                                                | 64.9 ms: 1.05x slower                                                  |
| xml_etree_generate   | 89.2 ms                                                | 95.6 ms: 1.07x slower                                                  |
| tomli_loads          | 2.33 sec                                               | 2.63 sec: 1.13x slower                                                 |
| unpickle_pure_python | 230 us                                                 | 334 us: 1.45x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.4 ms: 1.13x slower                                                  |
| django_template | 34.6 ms                                                | 43.2 ms: 1.25x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 124 us: 1.27x faster                                                   |
| async_tree_none            | 472 ms                                                 | 380 ms: 1.24x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 365 ms: 1.23x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 475 ms: 1.21x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 1.00 sec: 1.18x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 996 ms: 1.16x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 501 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 638 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 639 ms: 1.14x faster                                                   |
| pathlib                    | 19.3 ms                                                | 18.4 ms: 1.05x faster                                                  |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                                   |
| gc_traversal               | 3.79 ms                                                | 3.64 ms: 1.04x faster                                                  |
| json_loads                 | 28.5 us                                                | 27.5 us: 1.04x faster                                                  |
| coroutines                 | 23.2 ms                                                | 22.3 ms: 1.04x faster                                                  |
| unpickle_list              | 5.29 us                                                | 5.12 us: 1.03x faster                                                  |
| pickle_dict                | 35.5 us                                                | 34.5 us: 1.03x faster                                                  |
| generators                 | 31.2 ms                                                | 30.3 ms: 1.03x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 317 us: 1.02x faster                                                   |
| json                       | 5.26 ms                                                | 5.17 ms: 1.02x faster                                                  |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| pickle_list                | 5.08 us                                                | 5.15 us: 1.01x slower                                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.42 us: 1.02x slower                                                  |
| logging_format             | 7.23 us                                                | 7.41 us: 1.02x slower                                                  |
| logging_silent             | 104 ns                                                 | 107 ns: 1.03x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                  |
| xml_etree_iterparse        | 107 ms                                                 | 110 ms: 1.03x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 568 ms: 1.03x slower                                                   |
| regex_dna                  | 212 ms                                                 | 219 ms: 1.03x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| dask                       | 372 ms                                                 | 384 ms: 1.03x slower                                                   |
| logging_simple             | 6.46 us                                                | 6.69 us: 1.04x slower                                                  |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                 |
| async_generators           | 463 ms                                                 | 485 ms: 1.05x slower                                                   |
| pidigits                   | 187 ms                                                 | 196 ms: 1.05x slower                                                   |
| xml_etree_process          | 61.7 ms                                                | 64.9 ms: 1.05x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.80 ms: 1.05x slower                                                  |
| deepcopy                   | 371 us                                                 | 392 us: 1.06x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 519 ms: 1.06x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 181 ms: 1.07x slower                                                   |
| chameleon                  | 7.41 ms                                                | 7.93 ms: 1.07x slower                                                  |
| xml_etree_generate         | 89.2 ms                                                | 95.6 ms: 1.07x slower                                                  |
| regex_v8                   | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.34 ms: 1.08x slower                                                  |
| float                      | 84.7 ms                                                | 91.6 ms: 1.08x slower                                                  |
| bench_thread_pool          | 842 us                                                 | 910 us: 1.08x slower                                                   |
| aiohttp                    | 1.15 ms                                                | 1.25 ms: 1.09x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 3.08 us: 1.09x slower                                                  |
| meteor_contest             | 112 ms                                                 | 123 ms: 1.09x slower                                                   |
| dulwich_log                | 68.5 ms                                                | 75.4 ms: 1.10x slower                                                  |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| sympy_str                  | 300 ms                                                 | 331 ms: 1.10x slower                                                   |
| pycparser                  | 1.18 sec                                               | 1.31 sec: 1.11x slower                                                 |
| sympy_integrate            | 21.4 ms                                                | 23.8 ms: 1.11x slower                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.87 ms: 1.11x slower                                                  |
| mdp                        | 2.63 sec                                               | 2.93 sec: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.67 ms: 1.12x slower                                                  |
| raytrace                   | 312 ms                                                 | 352 ms: 1.13x slower                                                   |
| tomli_loads                | 2.33 sec                                               | 2.63 sec: 1.13x slower                                                 |
| mako                       | 11.9 ms                                                | 13.4 ms: 1.13x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.54 ms: 1.13x slower                                                  |
| docutils                   | 2.77 sec                                               | 3.14 sec: 1.13x slower                                                 |
| crypto_pyaes               | 81.9 ms                                                | 93.0 ms: 1.14x slower                                                  |
| 2to3                       | 274 ms                                                 | 313 ms: 1.14x slower                                                   |
| sympy_expand               | 478 ms                                                 | 548 ms: 1.15x slower                                                   |
| sqlglot_normalize          | 110 ms                                                 | 128 ms: 1.16x slower                                                   |
| deltablue                  | 3.72 ms                                                | 4.33 ms: 1.16x slower                                                  |
| comprehensions             | 21.8 us                                                | 25.6 us: 1.18x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                  |
| deepcopy_memo              | 40.7 us                                                | 48.9 us: 1.20x slower                                                  |
| chaos                      | 67.0 ms                                                | 80.8 ms: 1.21x slower                                                  |
| sqlglot_optimize           | 54.8 ms                                                | 66.2 ms: 1.21x slower                                                  |
| nbody                      | 97.0 ms                                                | 117 ms: 1.21x slower                                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 92.3 ms: 1.23x slower                                                  |
| django_template            | 34.6 ms                                                | 43.2 ms: 1.25x slower                                                  |
| scimark_sor                | 129 ms                                                 | 162 ms: 1.25x slower                                                   |
| richards                   | 45.8 ms                                                | 58.3 ms: 1.27x slower                                                  |
| richards_super             | 51.5 ms                                                | 65.7 ms: 1.28x slower                                                  |
| regex_compile              | 148 ms                                                 | 190 ms: 1.28x slower                                                   |
| fannkuch                   | 417 ms                                                 | 537 ms: 1.29x slower                                                   |
| pyflate                    | 482 ms                                                 | 633 ms: 1.31x slower                                                   |
| coverage                   | 72.7 ms                                                | 96.9 ms: 1.33x slower                                                  |
| telco                      | 7.10 ms                                                | 9.47 ms: 1.33x slower                                                  |
| go                         | 139 ms                                                 | 194 ms: 1.39x slower                                                   |
| scimark_fft                | 382 ms                                                 | 543 ms: 1.42x slower                                                   |
| pprint_safe_repr           | 776 ms                                                 | 1.12 sec: 1.44x slower                                                 |
| unpickle_pure_python       | 230 us                                                 | 334 us: 1.45x slower                                                   |
| scimark_lu                 | 118 ms                                                 | 172 ms: 1.45x slower                                                   |
| pprint_pformat             | 1.57 sec                                               | 2.31 sec: 1.47x slower                                                 |
| nqueens                    | 83.3 ms                                                | 125 ms: 1.50x slower                                                   |
| hexiom                     | 6.41 ms                                                | 10.3 ms: 1.60x slower                                                  |
| spectral_norm              | 115 ms                                                 | 203 ms: 1.76x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (4): mypy2, bench_mp_pool, unpickle, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.97x
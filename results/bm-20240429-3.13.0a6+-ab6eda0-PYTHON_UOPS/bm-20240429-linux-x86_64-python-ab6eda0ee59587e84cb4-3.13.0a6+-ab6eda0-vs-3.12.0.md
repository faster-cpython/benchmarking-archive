# Results vs. 3.12.0

- fork: python
- ref: ab6eda0ee59587e84cb4
- machine: linux-x86_64
- commit hash: ab6eda0
- commit date: 2024-04-29
- overall geometric mean: 1.21x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 361 ms: 1.31x slower                                                   |
| chameleon      | 7.41 ms                                                | 8.68 ms: 1.17x slower                                                  |
| docutils       | 2.77 sec                                               | 3.37 sec: 1.22x slower                                                 |
| tornado_http   | 103 ms                                                 | 105 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 366 ms: 1.23x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 476 ms: 1.21x faster                                                   |
| async_tree_none            | 472 ms                                                 | 393 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 999 ms: 1.18x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 1.00 sec: 1.16x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 636 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 651 ms: 1.12x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 526 ms: 1.10x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.17x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 194 ms: 1.03x slower                                                   |
| float          | 84.7 ms                                                | 122 ms: 1.44x slower                                                   |
| nbody          | 97.0 ms                                                | 198 ms: 2.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.45x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                  |
| regex_dna      | 212 ms                                                 | 226 ms: 1.07x slower                                                   |
| regex_v8       | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                  |
| regex_compile  | 148 ms                                                 | 220 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 151 ms: 1.05x faster                                                   |
| unpickle             | 15.9 us                                                | 15.3 us: 1.04x faster                                                  |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                  |
| unpickle_list        | 5.29 us                                                | 5.13 us: 1.03x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 318 us: 1.02x faster                                                   |
| pickle_dict          | 35.5 us                                                | 35.3 us: 1.01x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.11 us: 1.01x slower                                                  |
| pickle               | 11.6 us                                                | 12.0 us: 1.03x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                  |
| xml_etree_generate   | 89.2 ms                                                | 104 ms: 1.16x slower                                                   |
| xml_etree_iterparse  | 107 ms                                                 | 126 ms: 1.18x slower                                                   |
| xml_etree_process    | 61.7 ms                                                | 74.1 ms: 1.20x slower                                                  |
| tomli_loads          | 2.33 sec                                               | 3.38 sec: 1.45x slower                                                 |
| unpickle_pure_python | 230 us                                                 | 396 us: 1.72x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.19 ms: 1.04x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.6 ms                                                | 47.3 ms: 1.37x slower                                                  |
| mako            | 11.9 ms                                                | 20.3 ms: 1.71x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.53x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 366 ms: 1.23x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 476 ms: 1.21x faster                                                   |
| async_tree_none            | 472 ms                                                 | 393 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 999 ms: 1.18x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 1.00 sec: 1.16x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 636 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 651 ms: 1.12x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 526 ms: 1.10x faster                                                   |
| xml_etree_parse            | 159 ms                                                 | 151 ms: 1.05x faster                                                   |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.04x faster                                                  |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                  |
| unpickle_list              | 5.29 us                                                | 5.13 us: 1.03x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 318 us: 1.02x faster                                                   |
| pathlib                    | 19.3 ms                                                | 19.2 ms: 1.01x faster                                                  |
| json                       | 5.26 ms                                                | 5.21 ms: 1.01x faster                                                  |
| pickle_dict                | 35.5 us                                                | 35.3 us: 1.01x faster                                                  |
| pickle_list                | 5.08 us                                                | 5.11 us: 1.01x slower                                                  |
| generators                 | 31.2 ms                                                | 31.8 ms: 1.02x slower                                                  |
| tornado_http               | 103 ms                                                 | 105 ms: 1.03x slower                                                   |
| logging_silent             | 104 ns                                                 | 108 ns: 1.03x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 568 ms: 1.03x slower                                                   |
| pickle                     | 11.6 us                                                | 12.0 us: 1.03x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                  |
| pidigits                   | 187 ms                                                 | 194 ms: 1.03x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.19 ms: 1.04x slower                                                  |
| gc_traversal               | 3.79 ms                                                | 3.93 ms: 1.04x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                  |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.88 sec: 1.05x slower                                                 |
| coroutines                 | 23.2 ms                                                | 24.5 ms: 1.06x slower                                                  |
| regex_dna                  | 212 ms                                                 | 226 ms: 1.07x slower                                                   |
| dask                       | 372 ms                                                 | 397 ms: 1.07x slower                                                   |
| async_generators           | 463 ms                                                 | 496 ms: 1.07x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 530 ms: 1.08x slower                                                   |
| logging_format             | 7.23 us                                                | 7.88 us: 1.09x slower                                                  |
| logging_simple             | 6.46 us                                                | 7.08 us: 1.10x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 3.11 us: 1.10x slower                                                  |
| deepcopy                   | 371 us                                                 | 409 us: 1.10x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.37 ms: 1.11x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.28 ms: 1.11x slower                                                  |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                  |
| dulwich_log                | 68.5 ms                                                | 77.4 ms: 1.13x slower                                                  |
| sympy_sum                  | 169 ms                                                 | 192 ms: 1.13x slower                                                   |
| pycparser                  | 1.18 sec                                               | 1.34 sec: 1.14x slower                                                 |
| sqlglot_transpile          | 1.68 ms                                                | 1.94 ms: 1.15x slower                                                  |
| bench_thread_pool          | 842 us                                                 | 973 us: 1.16x slower                                                   |
| xml_etree_generate         | 89.2 ms                                                | 104 ms: 1.16x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                                  |
| chameleon                  | 7.41 ms                                                | 8.68 ms: 1.17x slower                                                  |
| xml_etree_iterparse        | 107 ms                                                 | 126 ms: 1.18x slower                                                   |
| mdp                        | 2.63 sec                                               | 3.13 sec: 1.19x slower                                                 |
| sympy_str                  | 300 ms                                                 | 360 ms: 1.20x slower                                                   |
| xml_etree_process          | 61.7 ms                                                | 74.1 ms: 1.20x slower                                                  |
| raytrace                   | 312 ms                                                 | 376 ms: 1.20x slower                                                   |
| docutils                   | 2.77 sec                                               | 3.37 sec: 1.22x slower                                                 |
| create_gc_cycles           | 1.48 ms                                                | 1.81 ms: 1.22x slower                                                  |
| sympy_expand               | 478 ms                                                 | 585 ms: 1.22x slower                                                   |
| deepcopy_memo              | 40.7 us                                                | 50.1 us: 1.23x slower                                                  |
| meteor_contest             | 112 ms                                                 | 143 ms: 1.27x slower                                                   |
| coverage                   | 72.7 ms                                                | 92.7 ms: 1.28x slower                                                  |
| sqlglot_normalize          | 110 ms                                                 | 142 ms: 1.29x slower                                                   |
| sympy_integrate            | 21.4 ms                                                | 27.7 ms: 1.29x slower                                                  |
| 2to3                       | 274 ms                                                 | 361 ms: 1.31x slower                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 73.5 ms: 1.34x slower                                                  |
| telco                      | 7.10 ms                                                | 9.64 ms: 1.36x slower                                                  |
| django_template            | 34.6 ms                                                | 47.3 ms: 1.37x slower                                                  |
| scimark_sor                | 129 ms                                                 | 178 ms: 1.38x slower                                                   |
| typing_runtime_protocols   | 158 us                                                 | 217 us: 1.38x slower                                                   |
| float                      | 84.7 ms                                                | 122 ms: 1.44x slower                                                   |
| tomli_loads                | 2.33 sec                                               | 3.38 sec: 1.45x slower                                                 |
| deltablue                  | 3.72 ms                                                | 5.41 ms: 1.46x slower                                                  |
| regex_compile              | 148 ms                                                 | 220 ms: 1.48x slower                                                   |
| crypto_pyaes               | 81.9 ms                                                | 122 ms: 1.49x slower                                                   |
| richards_super             | 51.5 ms                                                | 78.6 ms: 1.53x slower                                                  |
| chaos                      | 67.0 ms                                                | 103 ms: 1.54x slower                                                   |
| scimark_fft                | 382 ms                                                 | 596 ms: 1.56x slower                                                   |
| richards                   | 45.8 ms                                                | 71.6 ms: 1.56x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 8.26 ms: 1.63x slower                                                  |
| pprint_safe_repr           | 776 ms                                                 | 1.28 sec: 1.66x slower                                                 |
| fannkuch                   | 417 ms                                                 | 693 ms: 1.66x slower                                                   |
| pprint_pformat             | 1.57 sec                                               | 2.65 sec: 1.69x slower                                                 |
| scimark_lu                 | 118 ms                                                 | 201 ms: 1.71x slower                                                   |
| comprehensions             | 21.8 us                                                | 37.2 us: 1.71x slower                                                  |
| mako                       | 11.9 ms                                                | 20.3 ms: 1.71x slower                                                  |
| pyflate                    | 482 ms                                                 | 828 ms: 1.72x slower                                                   |
| unpickle_pure_python       | 230 us                                                 | 396 us: 1.72x slower                                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 134 ms: 1.78x slower                                                   |
| nqueens                    | 83.3 ms                                                | 151 ms: 1.81x slower                                                   |
| spectral_norm              | 115 ms                                                 | 211 ms: 1.84x slower                                                   |
| go                         | 139 ms                                                 | 260 ms: 1.87x slower                                                   |
| nbody                      | 97.0 ms                                                | 198 ms: 2.04x slower                                                   |
| hexiom                     | 6.41 ms                                                | 15.0 ms: 2.35x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.21x slower                                                           |

Benchmark hidden because not significant (3): deepcopy_reduce, bench_mp_pool, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240429-3.13.0a6+-ab6eda0-PYTHON_UOPS/bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 0.97x
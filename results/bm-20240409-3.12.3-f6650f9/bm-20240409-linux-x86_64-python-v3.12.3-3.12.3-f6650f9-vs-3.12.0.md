# Results vs. 3.12.0

- fork: python
- ref: v3.12.3
- machine: linux-x86_64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.02x faster
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 266 ms: 1.03x faster                                   |
| chameleon      | 7.41 ms                                                | 6.94 ms: 1.07x faster                                  |
| docutils       | 2.77 sec                                               | 2.73 sec: 1.01x faster                                 |
| tornado_http   | 103 ms                                                 | 96.9 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 455 ms: 1.01x slower                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 736 ms: 1.01x slower                                   |
| async_tree_memoization     | 578 ms                                                 | 586 ms: 1.02x slower                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 584 ms: 1.02x slower                                   |
| async_tree_none            | 472 ms                                                 | 481 ms: 1.02x slower                                   |
| async_tree_io              | 1.16 sec                                               | 1.18 sec: 1.02x slower                                 |
| async_tree_io_tg           | 1.18 sec                                               | 1.22 sec: 1.03x slower                                 |
| Geometric mean             | (ref)                                                  | 1.02x slower                                           |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 93.1 ms: 1.04x faster                                  |
| float          | 84.7 ms                                                | 83.5 ms: 1.01x faster                                  |
| pidigits       | 187 ms                                                 | 197 ms: 1.05x slower                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 140 ms: 1.06x faster                                   |
| regex_dna      | 212 ms                                                 | 211 ms: 1.01x faster                                   |
| regex_v8       | 23.1 ms                                                | 23.3 ms: 1.01x slower                                  |
| regex_effbot   | 3.61 ms                                                | 3.77 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| unpickle_list        | 5.29 us                                                | 5.04 us: 1.05x faster                                  |
| tomli_loads          | 2.33 sec                                               | 2.23 sec: 1.04x faster                                 |
| unpickle_pure_python | 230 us                                                 | 221 us: 1.04x faster                                   |
| pickle_pure_python   | 324 us                                                 | 313 us: 1.03x faster                                   |
| xml_etree_process    | 61.7 ms                                                | 60.1 ms: 1.03x faster                                  |
| pickle_dict          | 35.5 us                                                | 35.1 us: 1.01x faster                                  |
| pickle_list          | 5.08 us                                                | 5.05 us: 1.01x faster                                  |
| xml_etree_generate   | 89.2 ms                                                | 88.9 ms: 1.00x faster                                  |
| pickle               | 11.6 us                                                | 11.7 us: 1.00x slower                                  |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                   |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.02x slower                                   |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                  |
| json_loads           | 28.5 us                                                | 29.9 us: 1.05x slower                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 6.87 ms: 1.01x faster                                  |
| python_startup         | 9.55 ms                                                | 9.54 ms: 1.00x faster                                  |
| Geometric mean         | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.1 ms: 1.07x faster                                  |
| django_template | 34.6 ms                                                | 34.2 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| comprehensions             | 21.8 us                                                | 16.4 us: 1.33x faster                                  |
| typing_runtime_protocols   | 158 us                                                 | 119 us: 1.32x faster                                   |
| mypy2                      | 830 ms                                                 | 694 ms: 1.20x faster                                   |
| deltablue                  | 3.72 ms                                                | 3.23 ms: 1.15x faster                                  |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                   |
| generators                 | 31.2 ms                                                | 28.6 ms: 1.09x faster                                  |
| sympy_str                  | 300 ms                                                 | 274 ms: 1.09x faster                                   |
| logging_silent             | 104 ns                                                 | 96.6 ns: 1.08x faster                                  |
| richards                   | 45.8 ms                                                | 42.5 ms: 1.08x faster                                  |
| logging_format             | 7.23 us                                                | 6.73 us: 1.07x faster                                  |
| sympy_integrate            | 21.4 ms                                                | 20.0 ms: 1.07x faster                                  |
| mako                       | 11.9 ms                                                | 11.1 ms: 1.07x faster                                  |
| chameleon                  | 7.41 ms                                                | 6.94 ms: 1.07x faster                                  |
| deepcopy_memo              | 40.7 us                                                | 38.2 us: 1.07x faster                                  |
| regex_compile              | 148 ms                                                 | 140 ms: 1.06x faster                                   |
| tornado_http               | 103 ms                                                 | 96.9 ms: 1.06x faster                                  |
| logging_simple             | 6.46 us                                                | 6.12 us: 1.06x faster                                  |
| richards_super             | 51.5 ms                                                | 48.9 ms: 1.05x faster                                  |
| pyflate                    | 482 ms                                                 | 458 ms: 1.05x faster                                   |
| unpickle_list              | 5.29 us                                                | 5.04 us: 1.05x faster                                  |
| raytrace                   | 312 ms                                                 | 297 ms: 1.05x faster                                   |
| deepcopy                   | 371 us                                                 | 354 us: 1.05x faster                                   |
| pprint_safe_repr           | 776 ms                                                 | 742 ms: 1.05x faster                                   |
| tomli_loads                | 2.33 sec                                               | 2.23 sec: 1.04x faster                                 |
| nbody                      | 97.0 ms                                                | 93.1 ms: 1.04x faster                                  |
| unpickle_pure_python       | 230 us                                                 | 221 us: 1.04x faster                                   |
| dulwich_log                | 68.5 ms                                                | 66.0 ms: 1.04x faster                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.22 us: 1.04x faster                                  |
| fannkuch                   | 417 ms                                                 | 402 ms: 1.04x faster                                   |
| sqlalchemy_imperative      | 18.7 ms                                                | 18.0 ms: 1.04x faster                                  |
| sympy_expand               | 478 ms                                                 | 462 ms: 1.03x faster                                   |
| pickle_pure_python         | 324 us                                                 | 313 us: 1.03x faster                                   |
| pprint_pformat             | 1.57 sec                                               | 1.52 sec: 1.03x faster                                 |
| chaos                      | 67.0 ms                                                | 64.9 ms: 1.03x faster                                  |
| go                         | 139 ms                                                 | 135 ms: 1.03x faster                                   |
| sqlglot_normalize          | 110 ms                                                 | 107 ms: 1.03x faster                                   |
| 2to3                       | 274 ms                                                 | 266 ms: 1.03x faster                                   |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                  |
| xml_etree_process          | 61.7 ms                                                | 60.1 ms: 1.03x faster                                  |
| nqueens                    | 83.3 ms                                                | 81.2 ms: 1.03x faster                                  |
| spectral_norm              | 115 ms                                                 | 112 ms: 1.02x faster                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 73.4 ms: 1.02x faster                                  |
| scimark_sor                | 129 ms                                                 | 126 ms: 1.02x faster                                   |
| hexiom                     | 6.41 ms                                                | 6.27 ms: 1.02x faster                                  |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.02x faster                                   |
| gc_traversal               | 3.79 ms                                                | 3.73 ms: 1.02x faster                                  |
| sqlglot_optimize           | 54.8 ms                                                | 53.9 ms: 1.02x faster                                  |
| dask                       | 372 ms                                                 | 366 ms: 1.02x faster                                   |
| aiohttp                    | 1.15 ms                                                | 1.13 ms: 1.02x faster                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.98 ms: 1.02x faster                                  |
| float                      | 84.7 ms                                                | 83.5 ms: 1.01x faster                                  |
| async_generators           | 463 ms                                                 | 457 ms: 1.01x faster                                   |
| pickle_dict                | 35.5 us                                                | 35.1 us: 1.01x faster                                  |
| gunicorn                   | 1.24 ms                                                | 1.22 ms: 1.01x faster                                  |
| docutils                   | 2.77 sec                                               | 2.73 sec: 1.01x faster                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.34 ms: 1.01x faster                                  |
| django_template            | 34.6 ms                                                | 34.2 ms: 1.01x faster                                  |
| scimark_fft                | 382 ms                                                 | 378 ms: 1.01x faster                                   |
| sqlalchemy_declarative     | 147 ms                                                 | 145 ms: 1.01x faster                                   |
| python_startup_no_site     | 6.94 ms                                                | 6.87 ms: 1.01x faster                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.67 ms: 1.01x faster                                  |
| pickle_list                | 5.08 us                                                | 5.05 us: 1.01x faster                                  |
| regex_dna                  | 212 ms                                                 | 211 ms: 1.01x faster                                   |
| pycparser                  | 1.18 sec                                               | 1.17 sec: 1.01x faster                                 |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                  |
| bench_thread_pool          | 842 us                                                 | 838 us: 1.00x faster                                   |
| xml_etree_generate         | 89.2 ms                                                | 88.9 ms: 1.00x faster                                  |
| python_startup             | 9.55 ms                                                | 9.54 ms: 1.00x faster                                  |
| pickle                     | 11.6 us                                                | 11.7 us: 1.00x slower                                  |
| regex_v8                   | 23.1 ms                                                | 23.3 ms: 1.01x slower                                  |
| sqlite_synth               | 2.83 us                                                | 2.86 us: 1.01x slower                                  |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                   |
| async_tree_none_tg         | 450 ms                                                 | 455 ms: 1.01x slower                                   |
| json                       | 5.26 ms                                                | 5.33 ms: 1.01x slower                                  |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 736 ms: 1.01x slower                                   |
| async_tree_memoization     | 578 ms                                                 | 586 ms: 1.02x slower                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 584 ms: 1.02x slower                                   |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.02x slower                                   |
| async_tree_none            | 472 ms                                                 | 481 ms: 1.02x slower                                   |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                  |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                   |
| async_tree_io              | 1.16 sec                                               | 1.18 sec: 1.02x slower                                 |
| scimark_lu                 | 118 ms                                                 | 121 ms: 1.03x slower                                   |
| async_tree_io_tg           | 1.18 sec                                               | 1.22 sec: 1.03x slower                                 |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                 |
| crypto_pyaes               | 81.9 ms                                                | 84.3 ms: 1.03x slower                                  |
| coverage                   | 72.7 ms                                                | 75.2 ms: 1.03x slower                                  |
| telco                      | 7.10 ms                                                | 7.35 ms: 1.04x slower                                  |
| regex_effbot               | 3.61 ms                                                | 3.77 ms: 1.04x slower                                  |
| json_loads                 | 28.5 us                                                | 29.9 us: 1.05x slower                                  |
| pidigits                   | 187 ms                                                 | 197 ms: 1.05x slower                                   |
| asyncio_tcp                | 491 ms                                                 | 519 ms: 1.06x slower                                   |
| mdp                        | 2.63 sec                                               | 2.80 sec: 1.06x slower                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (4): create_gc_cycles, unpickle, coroutines, async_tree_cpu_io_mixed
Ignored benchmarks (1) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: unpack_sequence
Ignored benchmarks (6) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x
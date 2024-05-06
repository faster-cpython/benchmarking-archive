# Results vs. 3.12.0

- fork: gvanrossum
- ref: tier2_flag
- machine: linux-x86_64
- commit hash: 8cb71dd
- commit date: 2024-04-26
- overall geometric mean: 1.05x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 267 ms: 1.03x faster                                             |
| chameleon      | 7.41 ms                                                | 6.96 ms: 1.06x faster                                            |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                           |
| tornado_http   | 103 ms                                                 | 94.2 ms: 1.09x faster                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                             |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                             |
| async_tree_io_tg           | 1.18 sec                                               | 925 ms: 1.28x faster                                             |
| async_tree_io              | 1.16 sec                                               | 919 ms: 1.26x faster                                             |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                             |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 85.7 ms: 1.13x faster                                            |
| float          | 84.7 ms                                                | 77.5 ms: 1.09x faster                                            |
| pidigits       | 187 ms                                                 | 193 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                  | 1.06x faster                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 132 ms: 1.12x faster                                             |
| regex_effbot   | 3.61 ms                                                | 3.74 ms: 1.04x slower                                            |
| regex_dna      | 212 ms                                                 | 226 ms: 1.06x slower                                             |
| regex_v8       | 23.1 ms                                                | 25.7 ms: 1.11x slower                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.16 sec: 1.08x faster                                           |
| unpickle_pure_python | 230 us                                                 | 214 us: 1.08x faster                                             |
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                             |
| json_loads           | 28.5 us                                                | 27.8 us: 1.02x faster                                            |
| pickle_dict          | 35.5 us                                                | 34.7 us: 1.02x faster                                            |
| xml_etree_generate   | 89.2 ms                                                | 87.5 ms: 1.02x faster                                            |
| xml_etree_process    | 61.7 ms                                                | 60.6 ms: 1.02x faster                                            |
| unpickle_list        | 5.29 us                                                | 5.23 us: 1.01x faster                                            |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                            |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                            |
| unpickle             | 15.9 us                                                | 16.1 us: 1.02x slower                                            |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                     |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.7 ms: 1.11x faster                                            |
| django_template | 34.6 ms                                                | 34.8 ms: 1.01x slower                                            |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                             |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                             |
| comprehensions             | 21.8 us                                                | 16.3 us: 1.34x faster                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                             |
| async_tree_io_tg           | 1.18 sec                                               | 925 ms: 1.28x faster                                             |
| async_tree_io              | 1.16 sec                                               | 919 ms: 1.26x faster                                             |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                             |
| raytrace                   | 312 ms                                                 | 259 ms: 1.21x faster                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                             |
| deltablue                  | 3.72 ms                                                | 3.16 ms: 1.18x faster                                            |
| logging_format             | 7.23 us                                                | 6.33 us: 1.14x faster                                            |
| logging_simple             | 6.46 us                                                | 5.70 us: 1.13x faster                                            |
| chaos                      | 67.0 ms                                                | 59.1 ms: 1.13x faster                                            |
| mypy2                      | 830 ms                                                 | 733 ms: 1.13x faster                                             |
| nbody                      | 97.0 ms                                                | 85.7 ms: 1.13x faster                                            |
| regex_compile              | 148 ms                                                 | 132 ms: 1.12x faster                                             |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                            |
| deepcopy_memo              | 40.7 us                                                | 36.8 us: 1.11x faster                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 67.9 ms: 1.11x faster                                            |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                            |
| crypto_pyaes               | 81.9 ms                                                | 74.7 ms: 1.10x faster                                            |
| float                      | 84.7 ms                                                | 77.5 ms: 1.09x faster                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                             |
| tornado_http               | 103 ms                                                 | 94.2 ms: 1.09x faster                                            |
| scimark_sor                | 129 ms                                                 | 119 ms: 1.08x faster                                             |
| sympy_str                  | 300 ms                                                 | 277 ms: 1.08x faster                                             |
| tomli_loads                | 2.33 sec                                               | 2.16 sec: 1.08x faster                                           |
| hexiom                     | 6.41 ms                                                | 5.95 ms: 1.08x faster                                            |
| unpickle_pure_python       | 230 us                                                 | 214 us: 1.08x faster                                             |
| fannkuch                   | 417 ms                                                 | 389 ms: 1.07x faster                                             |
| generators                 | 31.2 ms                                                | 29.2 ms: 1.07x faster                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.58 ms: 1.07x faster                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.07x faster                                            |
| chameleon                  | 7.41 ms                                                | 6.96 ms: 1.06x faster                                            |
| pyflate                    | 482 ms                                                 | 453 ms: 1.06x faster                                             |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                             |
| deepcopy                   | 371 us                                                 | 350 us: 1.06x faster                                             |
| nqueens                    | 83.3 ms                                                | 78.8 ms: 1.06x faster                                            |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.06x faster                                            |
| scimark_fft                | 382 ms                                                 | 362 ms: 1.05x faster                                             |
| pprint_safe_repr           | 776 ms                                                 | 738 ms: 1.05x faster                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.19 us: 1.05x faster                                            |
| logging_silent             | 104 ns                                                 | 99.7 ns: 1.05x faster                                            |
| async_generators           | 463 ms                                                 | 442 ms: 1.05x faster                                             |
| scimark_lu                 | 118 ms                                                 | 113 ms: 1.04x faster                                             |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                           |
| meteor_contest             | 112 ms                                                 | 108 ms: 1.04x faster                                             |
| spectral_norm              | 115 ms                                                 | 111 ms: 1.03x faster                                             |
| 2to3                       | 274 ms                                                 | 267 ms: 1.03x faster                                             |
| dulwich_log                | 68.5 ms                                                | 66.7 ms: 1.03x faster                                            |
| bench_thread_pool          | 842 us                                                 | 820 us: 1.03x faster                                             |
| json                       | 5.26 ms                                                | 5.13 ms: 1.03x faster                                            |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.02x faster                                            |
| pickle_dict                | 35.5 us                                                | 34.7 us: 1.02x faster                                            |
| sympy_expand               | 478 ms                                                 | 469 ms: 1.02x faster                                             |
| xml_etree_generate         | 89.2 ms                                                | 87.5 ms: 1.02x faster                                            |
| xml_etree_process          | 61.7 ms                                                | 60.6 ms: 1.02x faster                                            |
| unpickle_list              | 5.29 us                                                | 5.23 us: 1.01x faster                                            |
| sqlglot_normalize          | 110 ms                                                 | 109 ms: 1.01x faster                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                            |
| sqlglot_optimize           | 54.8 ms                                                | 54.6 ms: 1.00x faster                                            |
| go                         | 139 ms                                                 | 140 ms: 1.00x slower                                             |
| django_template            | 34.6 ms                                                | 34.8 ms: 1.01x slower                                            |
| pickle_list                | 5.08 us                                                | 5.12 us: 1.01x slower                                            |
| coroutines                 | 23.2 ms                                                | 23.4 ms: 1.01x slower                                            |
| pycparser                  | 1.18 sec                                               | 1.19 sec: 1.01x slower                                           |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                            |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                           |
| unpickle                   | 15.9 us                                                | 16.1 us: 1.02x slower                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                            |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                            |
| richards                   | 45.8 ms                                                | 46.8 ms: 1.02x slower                                            |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                            |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                             |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                            |
| sqlite_synth               | 2.83 us                                                | 2.90 us: 1.03x slower                                            |
| pidigits                   | 187 ms                                                 | 193 ms: 1.03x slower                                             |
| mdp                        | 2.63 sec                                               | 2.71 sec: 1.03x slower                                           |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.03x slower                                           |
| regex_effbot               | 3.61 ms                                                | 3.74 ms: 1.04x slower                                            |
| typing_runtime_protocols   | 158 us                                                 | 163 us: 1.04x slower                                             |
| richards_super             | 51.5 ms                                                | 53.6 ms: 1.04x slower                                            |
| asyncio_tcp                | 491 ms                                                 | 515 ms: 1.05x slower                                             |
| gc_traversal               | 3.79 ms                                                | 4.02 ms: 1.06x slower                                            |
| regex_dna                  | 212 ms                                                 | 226 ms: 1.06x slower                                             |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                            |
| regex_v8                   | 23.1 ms                                                | 25.7 ms: 1.11x slower                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                            |
| telco                      | 7.10 ms                                                | 8.56 ms: 1.21x slower                                            |
| coverage                   | 72.7 ms                                                | 92.8 ms: 1.28x slower                                            |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                     |

Benchmark hidden because not significant (4): dask, xml_etree_iterparse, scimark_sparse_mat_mult, xml_etree_parse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240426-3.13.0a6+-8cb71dd/bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x
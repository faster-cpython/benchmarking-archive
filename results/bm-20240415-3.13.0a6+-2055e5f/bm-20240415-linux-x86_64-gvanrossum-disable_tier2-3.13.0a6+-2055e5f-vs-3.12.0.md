# Results vs. 3.12.0

- fork: gvanrossum
- ref: disable_tier2
- machine: linux-x86_64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 268 ms: 1.02x faster                                                |
| chameleon      | 7.41 ms                                                | 6.91 ms: 1.07x faster                                               |
| docutils       | 2.77 sec                                               | 2.79 sec: 1.01x slower                                              |
| tornado_http   | 103 ms                                                 | 94.3 ms: 1.09x faster                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 331 ms: 1.36x faster                                                |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 438 ms: 1.31x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 908 ms: 1.30x faster                                                |
| async_tree_io              | 1.16 sec                                               | 916 ms: 1.26x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 85.7 ms: 1.13x faster                                               |
| float          | 84.7 ms                                                | 77.7 ms: 1.09x faster                                               |
| pidigits       | 187 ms                                                 | 198 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                  | 1.05x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                |
| regex_effbot   | 3.61 ms                                                | 3.82 ms: 1.06x slower                                               |
| regex_dna      | 212 ms                                                 | 226 ms: 1.07x slower                                                |
| regex_v8       | 23.1 ms                                                | 25.9 ms: 1.12x slower                                               |
| Geometric mean | (ref)                                                  | 1.03x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.09 sec: 1.11x faster                                              |
| pickle_pure_python   | 324 us                                                 | 298 us: 1.09x faster                                                |
| unpickle_pure_python | 230 us                                                 | 212 us: 1.09x faster                                                |
| pickle_dict          | 35.5 us                                                | 34.0 us: 1.05x faster                                               |
| unpickle_list        | 5.29 us                                                | 5.07 us: 1.04x faster                                               |
| xml_etree_process    | 61.7 ms                                                | 59.9 ms: 1.03x faster                                               |
| xml_etree_generate   | 89.2 ms                                                | 86.9 ms: 1.03x faster                                               |
| json_loads           | 28.5 us                                                | 27.9 us: 1.02x faster                                               |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                               |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                               |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                               |
| unpickle             | 15.9 us                                                | 17.0 us: 1.07x slower                                               |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.12 ms: 1.03x slower                                               |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                               |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.8 ms: 1.11x faster                                               |
| django_template | 34.6 ms                                                | 34.4 ms: 1.00x faster                                               |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 115 us: 1.38x faster                                                |
| async_tree_none_tg         | 450 ms                                                 | 331 ms: 1.36x faster                                                |
| comprehensions             | 21.8 us                                                | 16.2 us: 1.35x faster                                               |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 438 ms: 1.31x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 908 ms: 1.30x faster                                                |
| async_tree_io              | 1.16 sec                                               | 916 ms: 1.26x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                |
| raytrace                   | 312 ms                                                 | 259 ms: 1.20x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                |
| deltablue                  | 3.72 ms                                                | 3.14 ms: 1.18x faster                                               |
| logging_format             | 7.23 us                                                | 6.26 us: 1.15x faster                                               |
| logging_simple             | 6.46 us                                                | 5.64 us: 1.14x faster                                               |
| nbody                      | 97.0 ms                                                | 85.7 ms: 1.13x faster                                               |
| chaos                      | 67.0 ms                                                | 59.5 ms: 1.13x faster                                               |
| mypy2                      | 830 ms                                                 | 738 ms: 1.12x faster                                                |
| scimark_monte_carlo        | 75.1 ms                                                | 67.3 ms: 1.12x faster                                               |
| tomli_loads                | 2.33 sec                                               | 2.09 sec: 1.11x faster                                              |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                |
| mako                       | 11.9 ms                                                | 10.8 ms: 1.11x faster                                               |
| deepcopy_memo              | 40.7 us                                                | 37.1 us: 1.10x faster                                               |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                                |
| crypto_pyaes               | 81.9 ms                                                | 74.8 ms: 1.09x faster                                               |
| float                      | 84.7 ms                                                | 77.7 ms: 1.09x faster                                               |
| tornado_http               | 103 ms                                                 | 94.3 ms: 1.09x faster                                               |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.09x faster                                               |
| pickle_pure_python         | 324 us                                                 | 298 us: 1.09x faster                                                |
| unpickle_pure_python       | 230 us                                                 | 212 us: 1.09x faster                                                |
| logging_silent             | 104 ns                                                 | 96.2 ns: 1.09x faster                                               |
| chameleon                  | 7.41 ms                                                | 6.91 ms: 1.07x faster                                               |
| sympy_str                  | 300 ms                                                 | 279 ms: 1.07x faster                                                |
| scimark_sor                | 129 ms                                                 | 120 ms: 1.07x faster                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.27 ms: 1.07x faster                                               |
| fannkuch                   | 417 ms                                                 | 391 ms: 1.07x faster                                                |
| generators                 | 31.2 ms                                                | 29.4 ms: 1.06x faster                                               |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                               |
| sympy_integrate            | 21.4 ms                                                | 20.2 ms: 1.06x faster                                               |
| deepcopy_reduce            | 3.35 us                                                | 3.16 us: 1.06x faster                                               |
| deepcopy                   | 371 us                                                 | 351 us: 1.06x faster                                                |
| nqueens                    | 83.3 ms                                                | 79.6 ms: 1.05x faster                                               |
| pickle_dict                | 35.5 us                                                | 34.0 us: 1.05x faster                                               |
| hexiom                     | 6.41 ms                                                | 6.13 ms: 1.05x faster                                               |
| async_generators           | 463 ms                                                 | 444 ms: 1.04x faster                                                |
| unpickle_list              | 5.29 us                                                | 5.07 us: 1.04x faster                                               |
| pyflate                    | 482 ms                                                 | 463 ms: 1.04x faster                                                |
| dulwich_log                | 68.5 ms                                                | 65.9 ms: 1.04x faster                                               |
| pprint_safe_repr           | 776 ms                                                 | 749 ms: 1.04x faster                                                |
| spectral_norm              | 115 ms                                                 | 111 ms: 1.04x faster                                                |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                |
| scimark_fft                | 382 ms                                                 | 369 ms: 1.03x faster                                                |
| xml_etree_process          | 61.7 ms                                                | 59.9 ms: 1.03x faster                                               |
| mdp                        | 2.63 sec                                               | 2.56 sec: 1.03x faster                                              |
| xml_etree_generate         | 89.2 ms                                                | 86.9 ms: 1.03x faster                                               |
| pprint_pformat             | 1.57 sec                                               | 1.53 sec: 1.02x faster                                              |
| scimark_lu                 | 118 ms                                                 | 115 ms: 1.02x faster                                                |
| 2to3                       | 274 ms                                                 | 268 ms: 1.02x faster                                                |
| json_loads                 | 28.5 us                                                | 27.9 us: 1.02x faster                                               |
| json                       | 5.26 ms                                                | 5.16 ms: 1.02x faster                                               |
| pickle_list                | 5.08 us                                                | 5.00 us: 1.02x faster                                               |
| sympy_expand               | 478 ms                                                 | 470 ms: 1.02x faster                                                |
| dask                       | 372 ms                                                 | 366 ms: 1.02x faster                                                |
| sqlglot_normalize          | 110 ms                                                 | 109 ms: 1.01x faster                                                |
| bench_thread_pool          | 842 us                                                 | 834 us: 1.01x faster                                                |
| django_template            | 34.6 ms                                                | 34.4 ms: 1.00x faster                                               |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                               |
| docutils                   | 2.77 sec                                               | 2.79 sec: 1.01x slower                                              |
| richards                   | 45.8 ms                                                | 46.3 ms: 1.01x slower                                               |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                |
| richards_super             | 51.5 ms                                                | 52.2 ms: 1.01x slower                                               |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                               |
| pycparser                  | 1.18 sec                                               | 1.20 sec: 1.02x slower                                              |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.17 ms: 1.02x slower                                               |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                               |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                               |
| python_startup_no_site     | 6.94 ms                                                | 7.12 ms: 1.03x slower                                               |
| asyncio_tcp                | 491 ms                                                 | 505 ms: 1.03x slower                                                |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                              |
| sqlite_synth               | 2.83 us                                                | 2.94 us: 1.04x slower                                               |
| gc_traversal               | 3.79 ms                                                | 4.01 ms: 1.06x slower                                               |
| regex_effbot               | 3.61 ms                                                | 3.82 ms: 1.06x slower                                               |
| pidigits                   | 187 ms                                                 | 198 ms: 1.06x slower                                                |
| regex_dna                  | 212 ms                                                 | 226 ms: 1.07x slower                                                |
| unpickle                   | 15.9 us                                                | 17.0 us: 1.07x slower                                               |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                               |
| regex_v8                   | 23.1 ms                                                | 25.9 ms: 1.12x slower                                               |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                               |
| telco                      | 7.10 ms                                                | 8.69 ms: 1.22x slower                                               |
| coverage                   | 72.7 ms                                                | 96.4 ms: 1.33x slower                                               |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                        |

Benchmark hidden because not significant (5): sqlglot_optimize, bench_mp_pool, coroutines, go, xml_etree_parse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240415-3.13.0a6+-2055e5f/bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x
# Results vs. 3.12.0

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.04x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 269 ms: 1.02x faster                                                |
| chameleon      | 7.41 ms                                                | 7.10 ms: 1.04x faster                                               |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                              |
| tornado_http   | 103 ms                                                 | 93.9 ms: 1.09x faster                                               |
| Geometric mean | (ref)                                                  | 1.03x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.33x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 915 ms: 1.29x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                |
| async_tree_io              | 1.16 sec                                               | 943 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.19x faster                                                |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 87.2 ms: 1.11x faster                                               |
| float          | 84.7 ms                                                | 78.3 ms: 1.08x faster                                               |
| pidigits       | 187 ms                                                 | 190 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                |
| regex_effbot   | 3.61 ms                                                | 3.73 ms: 1.03x slower                                               |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                |
| regex_v8       | 23.1 ms                                                | 25.0 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                  | 1.02x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 230 us                                                 | 214 us: 1.07x faster                                                |
| tomli_loads          | 2.33 sec                                               | 2.17 sec: 1.07x faster                                              |
| pickle_pure_python   | 324 us                                                 | 302 us: 1.07x faster                                                |
| unpickle_list        | 5.29 us                                                | 5.03 us: 1.05x faster                                               |
| pickle_dict          | 35.5 us                                                | 34.3 us: 1.04x faster                                               |
| json_loads           | 28.5 us                                                | 27.7 us: 1.03x faster                                               |
| xml_etree_generate   | 89.2 ms                                                | 87.8 ms: 1.02x faster                                               |
| xml_etree_process    | 61.7 ms                                                | 60.9 ms: 1.01x faster                                               |
| xml_etree_iterparse  | 107 ms                                                 | 107 ms: 1.01x slower                                                |
| pickle_list          | 5.08 us                                                | 5.13 us: 1.01x slower                                               |
| xml_etree_parse      | 159 ms                                                 | 161 ms: 1.01x slower                                                |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.02x slower                                               |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                               |
| unpickle             | 15.9 us                                                | 16.6 us: 1.05x slower                                               |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.08 ms: 1.02x slower                                               |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                               |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.7 ms: 1.11x faster                                               |
| django_template | 34.6 ms                                                | 35.5 ms: 1.03x slower                                               |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                                |
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.33x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                |
| comprehensions             | 21.8 us                                                | 16.8 us: 1.29x faster                                               |
| async_tree_io_tg           | 1.18 sec                                               | 915 ms: 1.29x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                |
| async_tree_io              | 1.16 sec                                               | 943 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.19x faster                                                |
| raytrace                   | 312 ms                                                 | 264 ms: 1.18x faster                                                |
| deltablue                  | 3.72 ms                                                | 3.21 ms: 1.16x faster                                               |
| mypy2                      | 830 ms                                                 | 736 ms: 1.13x faster                                                |
| crypto_pyaes               | 81.9 ms                                                | 73.5 ms: 1.11x faster                                               |
| nbody                      | 97.0 ms                                                | 87.2 ms: 1.11x faster                                               |
| logging_format             | 7.23 us                                                | 6.50 us: 1.11x faster                                               |
| chaos                      | 67.0 ms                                                | 60.5 ms: 1.11x faster                                               |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                               |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                |
| logging_simple             | 6.46 us                                                | 5.85 us: 1.10x faster                                               |
| scimark_monte_carlo        | 75.1 ms                                                | 68.2 ms: 1.10x faster                                               |
| deepcopy_memo              | 40.7 us                                                | 37.0 us: 1.10x faster                                               |
| tornado_http               | 103 ms                                                 | 93.9 ms: 1.09x faster                                               |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.09x faster                                               |
| float                      | 84.7 ms                                                | 78.3 ms: 1.08x faster                                               |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                |
| unpickle_pure_python       | 230 us                                                 | 214 us: 1.07x faster                                                |
| tomli_loads                | 2.33 sec                                               | 2.17 sec: 1.07x faster                                              |
| pickle_pure_python         | 324 us                                                 | 302 us: 1.07x faster                                                |
| sqlglot_transpile          | 1.68 ms                                                | 1.58 ms: 1.07x faster                                               |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.07x faster                                               |
| sympy_str                  | 300 ms                                                 | 282 ms: 1.06x faster                                                |
| fannkuch                   | 417 ms                                                 | 394 ms: 1.06x faster                                                |
| scimark_sor                | 129 ms                                                 | 123 ms: 1.05x faster                                                |
| unpickle_list              | 5.29 us                                                | 5.03 us: 1.05x faster                                               |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                               |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                               |
| hexiom                     | 6.41 ms                                                | 6.14 ms: 1.04x faster                                               |
| chameleon                  | 7.41 ms                                                | 7.10 ms: 1.04x faster                                               |
| deepcopy                   | 371 us                                                 | 356 us: 1.04x faster                                                |
| deepcopy_reduce            | 3.35 us                                                | 3.22 us: 1.04x faster                                               |
| pyflate                    | 482 ms                                                 | 465 ms: 1.04x faster                                                |
| logging_silent             | 104 ns                                                 | 101 ns: 1.04x faster                                                |
| dulwich_log                | 68.5 ms                                                | 66.0 ms: 1.04x faster                                               |
| pickle_dict                | 35.5 us                                                | 34.3 us: 1.04x faster                                               |
| async_generators           | 463 ms                                                 | 447 ms: 1.04x faster                                                |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                |
| gc_traversal               | 3.79 ms                                                | 3.68 ms: 1.03x faster                                               |
| json_loads                 | 28.5 us                                                | 27.7 us: 1.03x faster                                               |
| pprint_safe_repr           | 776 ms                                                 | 756 ms: 1.03x faster                                                |
| scimark_lu                 | 118 ms                                                 | 115 ms: 1.02x faster                                                |
| coroutines                 | 23.2 ms                                                | 22.7 ms: 1.02x faster                                               |
| 2to3                       | 274 ms                                                 | 269 ms: 1.02x faster                                                |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                              |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                              |
| nqueens                    | 83.3 ms                                                | 81.9 ms: 1.02x faster                                               |
| xml_etree_generate         | 89.2 ms                                                | 87.8 ms: 1.02x faster                                               |
| json                       | 5.26 ms                                                | 5.18 ms: 1.01x faster                                               |
| xml_etree_process          | 61.7 ms                                                | 60.9 ms: 1.01x faster                                               |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                |
| scimark_fft                | 382 ms                                                 | 378 ms: 1.01x faster                                                |
| bench_thread_pool          | 842 us                                                 | 836 us: 1.01x faster                                                |
| sympy_expand               | 478 ms                                                 | 475 ms: 1.01x faster                                                |
| sqlglot_normalize          | 110 ms                                                 | 111 ms: 1.01x slower                                                |
| xml_etree_iterparse        | 107 ms                                                 | 107 ms: 1.01x slower                                                |
| pickle_list                | 5.08 us                                                | 5.13 us: 1.01x slower                                               |
| sqlglot_optimize           | 54.8 ms                                                | 55.3 ms: 1.01x slower                                               |
| xml_etree_parse            | 159 ms                                                 | 161 ms: 1.01x slower                                                |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                               |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.02x slower                                               |
| pidigits                   | 187 ms                                                 | 190 ms: 1.02x slower                                                |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                              |
| mdp                        | 2.63 sec                                               | 2.68 sec: 1.02x slower                                              |
| python_startup_no_site     | 6.94 ms                                                | 7.08 ms: 1.02x slower                                               |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.17 ms: 1.02x slower                                               |
| richards_super             | 51.5 ms                                                | 52.7 ms: 1.02x slower                                               |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                               |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                               |
| django_template            | 34.6 ms                                                | 35.5 ms: 1.03x slower                                               |
| richards                   | 45.8 ms                                                | 47.3 ms: 1.03x slower                                               |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                              |
| asyncio_websockets         | 551 ms                                                 | 569 ms: 1.03x slower                                                |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                |
| regex_effbot               | 3.61 ms                                                | 3.73 ms: 1.03x slower                                               |
| unpickle                   | 15.9 us                                                | 16.6 us: 1.05x slower                                               |
| sqlite_synth               | 2.83 us                                                | 2.98 us: 1.05x slower                                               |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                |
| regex_v8                   | 23.1 ms                                                | 25.0 ms: 1.08x slower                                               |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                               |
| create_gc_cycles           | 1.48 ms                                                | 1.74 ms: 1.18x slower                                               |
| telco                      | 7.10 ms                                                | 8.71 ms: 1.23x slower                                               |
| coverage                   | 72.7 ms                                                | 98.0 ms: 1.35x slower                                               |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                        |

Benchmark hidden because not significant (2): bench_mp_pool, spectral_norm
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240417-3.13.0a6+-5e20f0f/bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x
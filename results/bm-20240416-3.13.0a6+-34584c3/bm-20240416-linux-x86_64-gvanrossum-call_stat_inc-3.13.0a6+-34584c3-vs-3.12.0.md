# Results vs. 3.12.0

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 34584c3
- commit date: 2024-04-16
- overall geometric mean: 1.04x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 271 ms: 1.01x faster                                                |
| chameleon      | 7.41 ms                                                | 6.96 ms: 1.06x faster                                               |
| docutils       | 2.77 sec                                               | 2.83 sec: 1.02x slower                                              |
| tornado_http   | 103 ms                                                 | 94.2 ms: 1.09x faster                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 922 ms: 1.28x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                |
| async_tree_io              | 1.16 sec                                               | 930 ms: 1.24x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 608 ms: 1.19x faster                                                |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.9 ms: 1.07x faster                                               |
| nbody          | 97.0 ms                                                | 91.1 ms: 1.06x faster                                               |
| pidigits       | 187 ms                                                 | 193 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 136 ms: 1.09x faster                                                |
| regex_effbot   | 3.61 ms                                                | 3.71 ms: 1.03x slower                                               |
| regex_dna      | 212 ms                                                 | 222 ms: 1.05x slower                                                |
| regex_v8       | 23.1 ms                                                | 24.9 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                  | 1.01x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 302 us: 1.07x faster                                                |
| tomli_loads          | 2.33 sec                                               | 2.21 sec: 1.05x faster                                              |
| unpickle_list        | 5.29 us                                                | 5.03 us: 1.05x faster                                               |
| unpickle_pure_python | 230 us                                                 | 220 us: 1.05x faster                                                |
| json_loads           | 28.5 us                                                | 27.8 us: 1.03x faster                                               |
| xml_etree_process    | 61.7 ms                                                | 60.8 ms: 1.02x faster                                               |
| xml_etree_generate   | 89.2 ms                                                | 88.7 ms: 1.01x faster                                               |
| pickle_dict          | 35.5 us                                                | 35.4 us: 1.00x faster                                               |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.02x slower                                                |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.02x slower                                                |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                               |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                               |
| pickle_list          | 5.08 us                                                | 5.40 us: 1.06x slower                                               |
| unpickle             | 15.9 us                                                | 17.0 us: 1.07x slower                                               |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.13 ms: 1.03x slower                                               |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.10x slower                                               |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.0 ms: 1.08x faster                                               |
| django_template | 34.6 ms                                                | 35.1 ms: 1.01x slower                                               |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 116 us: 1.36x faster                                                |
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 922 ms: 1.28x faster                                                |
| comprehensions             | 21.8 us                                                | 17.1 us: 1.27x faster                                               |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                |
| async_tree_io              | 1.16 sec                                               | 930 ms: 1.24x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 608 ms: 1.19x faster                                                |
| raytrace                   | 312 ms                                                 | 263 ms: 1.19x faster                                                |
| deltablue                  | 3.72 ms                                                | 3.29 ms: 1.13x faster                                               |
| logging_format             | 7.23 us                                                | 6.42 us: 1.13x faster                                               |
| mypy2                      | 830 ms                                                 | 741 ms: 1.12x faster                                                |
| logging_simple             | 6.46 us                                                | 5.78 us: 1.12x faster                                               |
| chaos                      | 67.0 ms                                                | 60.2 ms: 1.11x faster                                               |
| pathlib                    | 19.3 ms                                                | 17.5 ms: 1.10x faster                                               |
| scimark_monte_carlo        | 75.1 ms                                                | 68.5 ms: 1.10x faster                                               |
| crypto_pyaes               | 81.9 ms                                                | 74.7 ms: 1.10x faster                                               |
| regex_compile              | 148 ms                                                 | 136 ms: 1.09x faster                                                |
| tornado_http               | 103 ms                                                 | 94.2 ms: 1.09x faster                                               |
| mako                       | 11.9 ms                                                | 11.0 ms: 1.08x faster                                               |
| fannkuch                   | 417 ms                                                 | 387 ms: 1.08x faster                                                |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                |
| float                      | 84.7 ms                                                | 78.9 ms: 1.07x faster                                               |
| pickle_pure_python         | 324 us                                                 | 302 us: 1.07x faster                                                |
| nbody                      | 97.0 ms                                                | 91.1 ms: 1.06x faster                                               |
| chameleon                  | 7.41 ms                                                | 6.96 ms: 1.06x faster                                               |
| deepcopy_memo              | 40.7 us                                                | 38.3 us: 1.06x faster                                               |
| sympy_str                  | 300 ms                                                 | 282 ms: 1.06x faster                                                |
| scimark_sor                | 129 ms                                                 | 122 ms: 1.06x faster                                                |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.06x faster                                               |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.06x faster                                               |
| tomli_loads                | 2.33 sec                                               | 2.21 sec: 1.05x faster                                              |
| deepcopy_reduce            | 3.35 us                                                | 3.18 us: 1.05x faster                                               |
| unpickle_list              | 5.29 us                                                | 5.03 us: 1.05x faster                                               |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                               |
| deepcopy                   | 371 us                                                 | 354 us: 1.05x faster                                                |
| sympy_integrate            | 21.4 ms                                                | 20.5 ms: 1.05x faster                                               |
| async_generators           | 463 ms                                                 | 443 ms: 1.05x faster                                                |
| unpickle_pure_python       | 230 us                                                 | 220 us: 1.05x faster                                                |
| pyflate                    | 482 ms                                                 | 467 ms: 1.03x faster                                                |
| scimark_fft                | 382 ms                                                 | 370 ms: 1.03x faster                                                |
| pprint_safe_repr           | 776 ms                                                 | 754 ms: 1.03x faster                                                |
| dulwich_log                | 68.5 ms                                                | 66.7 ms: 1.03x faster                                               |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.03x faster                                               |
| scimark_lu                 | 118 ms                                                 | 115 ms: 1.03x faster                                                |
| logging_silent             | 104 ns                                                 | 102 ns: 1.02x faster                                                |
| nqueens                    | 83.3 ms                                                | 81.6 ms: 1.02x faster                                               |
| xml_etree_process          | 61.7 ms                                                | 60.8 ms: 1.02x faster                                               |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                              |
| mdp                        | 2.63 sec                                               | 2.59 sec: 1.01x faster                                              |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                |
| spectral_norm              | 115 ms                                                 | 113 ms: 1.01x faster                                                |
| 2to3                       | 274 ms                                                 | 271 ms: 1.01x faster                                                |
| sympy_expand               | 478 ms                                                 | 473 ms: 1.01x faster                                                |
| pprint_pformat             | 1.57 sec                                               | 1.55 sec: 1.01x faster                                              |
| coroutines                 | 23.2 ms                                                | 23.0 ms: 1.01x faster                                               |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                               |
| hexiom                     | 6.41 ms                                                | 6.37 ms: 1.01x faster                                               |
| xml_etree_generate         | 89.2 ms                                                | 88.7 ms: 1.01x faster                                               |
| bench_thread_pool          | 842 us                                                 | 838 us: 1.00x faster                                                |
| pickle_dict                | 35.5 us                                                | 35.4 us: 1.00x faster                                               |
| sqlglot_normalize          | 110 ms                                                 | 111 ms: 1.01x slower                                                |
| django_template            | 34.6 ms                                                | 35.1 ms: 1.01x slower                                               |
| sqlglot_optimize           | 54.8 ms                                                | 55.6 ms: 1.02x slower                                               |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.02x slower                                                |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.02x slower                                                |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                               |
| docutils                   | 2.77 sec                                               | 2.83 sec: 1.02x slower                                              |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.17 ms: 1.02x slower                                               |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                               |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.03x slower                                               |
| regex_effbot               | 3.61 ms                                                | 3.71 ms: 1.03x slower                                               |
| python_startup_no_site     | 6.94 ms                                                | 7.13 ms: 1.03x slower                                               |
| go                         | 139 ms                                                 | 143 ms: 1.03x slower                                                |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                              |
| pidigits                   | 187 ms                                                 | 193 ms: 1.03x slower                                                |
| asyncio_tcp                | 491 ms                                                 | 507 ms: 1.03x slower                                                |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                               |
| sqlite_synth               | 2.83 us                                                | 2.94 us: 1.04x slower                                               |
| gc_traversal               | 3.79 ms                                                | 3.96 ms: 1.04x slower                                               |
| regex_dna                  | 212 ms                                                 | 222 ms: 1.05x slower                                                |
| richards_super             | 51.5 ms                                                | 54.4 ms: 1.06x slower                                               |
| richards                   | 45.8 ms                                                | 48.4 ms: 1.06x slower                                               |
| pickle_list                | 5.08 us                                                | 5.40 us: 1.06x slower                                               |
| unpickle                   | 15.9 us                                                | 17.0 us: 1.07x slower                                               |
| regex_v8                   | 23.1 ms                                                | 24.9 ms: 1.08x slower                                               |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.10x slower                                               |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                               |
| telco                      | 7.10 ms                                                | 8.65 ms: 1.22x slower                                               |
| coverage                   | 72.7 ms                                                | 96.8 ms: 1.33x slower                                               |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                        |

Benchmark hidden because not significant (1): json
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240416-3.13.0a6+-34584c3/bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x
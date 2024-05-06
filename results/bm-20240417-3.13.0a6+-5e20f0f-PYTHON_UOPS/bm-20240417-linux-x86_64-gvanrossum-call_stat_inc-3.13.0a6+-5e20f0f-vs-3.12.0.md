# Results vs. 3.12.0

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.20x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 332 ms: 1.21x slower                                                |
| chameleon      | 7.41 ms                                                | 8.07 ms: 1.09x slower                                               |
| docutils       | 2.77 sec                                               | 3.28 sec: 1.19x slower                                              |
| tornado_http   | 103 ms                                                 | 104 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                  | 1.12x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 371 ms: 1.21x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 480 ms: 1.20x faster                                                |
| async_tree_none            | 472 ms                                                 | 400 ms: 1.18x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 1.01 sec: 1.17x faster                                              |
| async_tree_io              | 1.16 sec                                               | 995 ms: 1.16x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 649 ms: 1.12x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 660 ms: 1.10x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 529 ms: 1.09x faster                                                |
| Geometric mean             | (ref)                                                  | 1.15x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 195 ms: 1.04x slower                                                |
| float          | 84.7 ms                                                | 139 ms: 1.64x slower                                                |
| nbody          | 97.0 ms                                                | 203 ms: 2.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.53x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.88 ms: 1.08x slower                                               |
| regex_dna      | 212 ms                                                 | 235 ms: 1.11x slower                                                |
| regex_v8       | 23.1 ms                                                | 27.2 ms: 1.18x slower                                               |
| regex_compile  | 148 ms                                                 | 223 ms: 1.50x slower                                                |
| Geometric mean | (ref)                                                  | 1.20x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 314 us: 1.03x faster                                                |
| json_loads           | 28.5 us                                                | 27.9 us: 1.02x faster                                               |
| unpickle_list        | 5.29 us                                                | 5.24 us: 1.01x faster                                               |
| pickle_dict          | 35.5 us                                                | 35.8 us: 1.01x slower                                               |
| xml_etree_parse      | 159 ms                                                 | 163 ms: 1.02x slower                                                |
| pickle_list          | 5.08 us                                                | 5.20 us: 1.02x slower                                               |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                               |
| pickle               | 11.6 us                                                | 12.1 us: 1.04x slower                                               |
| unpickle             | 15.9 us                                                | 16.8 us: 1.06x slower                                               |
| xml_etree_process    | 61.7 ms                                                | 70.4 ms: 1.14x slower                                               |
| xml_etree_generate   | 89.2 ms                                                | 105 ms: 1.18x slower                                                |
| xml_etree_iterparse  | 107 ms                                                 | 133 ms: 1.25x slower                                                |
| tomli_loads          | 2.33 sec                                               | 3.41 sec: 1.46x slower                                              |
| unpickle_pure_python | 230 us                                                 | 406 us: 1.76x slower                                                |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.13 ms: 1.03x slower                                               |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                               |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| django_template | 34.6 ms                                                | 42.9 ms: 1.24x slower                                               |
| mako            | 11.9 ms                                                | 20.9 ms: 1.76x slower                                               |
| Geometric mean  | (ref)                                                  | 1.48x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 130 us: 1.22x faster                                                |
| async_tree_none_tg         | 450 ms                                                 | 371 ms: 1.21x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 480 ms: 1.20x faster                                                |
| async_tree_none            | 472 ms                                                 | 400 ms: 1.18x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 1.01 sec: 1.17x faster                                              |
| async_tree_io              | 1.16 sec                                               | 995 ms: 1.16x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 649 ms: 1.12x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 660 ms: 1.10x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 529 ms: 1.09x faster                                                |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                               |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                               |
| pickle_pure_python         | 324 us                                                 | 314 us: 1.03x faster                                                |
| json_loads                 | 28.5 us                                                | 27.9 us: 1.02x faster                                               |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                               |
| json                       | 5.26 ms                                                | 5.20 ms: 1.01x faster                                               |
| unpickle_list              | 5.29 us                                                | 5.24 us: 1.01x faster                                               |
| pickle_dict                | 35.5 us                                                | 35.8 us: 1.01x slower                                               |
| tornado_http               | 103 ms                                                 | 104 ms: 1.01x slower                                                |
| xml_etree_parse            | 159 ms                                                 | 163 ms: 1.02x slower                                                |
| deepcopy_reduce            | 3.35 us                                                | 3.41 us: 1.02x slower                                               |
| pickle_list                | 5.08 us                                                | 5.20 us: 1.02x slower                                               |
| logging_format             | 7.23 us                                                | 7.42 us: 1.03x slower                                               |
| python_startup_no_site     | 6.94 ms                                                | 7.13 ms: 1.03x slower                                               |
| asyncio_websockets         | 551 ms                                                 | 568 ms: 1.03x slower                                                |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                               |
| pidigits                   | 187 ms                                                 | 195 ms: 1.04x slower                                                |
| logging_simple             | 6.46 us                                                | 6.72 us: 1.04x slower                                               |
| gc_traversal               | 3.79 ms                                                | 3.95 ms: 1.04x slower                                               |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                              |
| dask                       | 372 ms                                                 | 388 ms: 1.04x slower                                                |
| pickle                     | 11.6 us                                                | 12.1 us: 1.04x slower                                               |
| asyncio_tcp                | 491 ms                                                 | 513 ms: 1.05x slower                                                |
| logging_silent             | 104 ns                                                 | 109 ns: 1.05x slower                                                |
| unpickle                   | 15.9 us                                                | 16.8 us: 1.06x slower                                               |
| deepcopy                   | 371 us                                                 | 395 us: 1.06x slower                                                |
| regex_effbot               | 3.61 ms                                                | 3.88 ms: 1.08x slower                                               |
| chameleon                  | 7.41 ms                                                | 8.07 ms: 1.09x slower                                               |
| async_generators           | 463 ms                                                 | 507 ms: 1.09x slower                                                |
| gunicorn                   | 1.24 ms                                                | 1.36 ms: 1.10x slower                                               |
| aiohttp                    | 1.15 ms                                                | 1.26 ms: 1.10x slower                                               |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                               |
| dulwich_log                | 68.5 ms                                                | 75.8 ms: 1.11x slower                                               |
| regex_dna                  | 212 ms                                                 | 235 ms: 1.11x slower                                                |
| bench_thread_pool          | 842 us                                                 | 933 us: 1.11x slower                                                |
| sqlite_synth               | 2.83 us                                                | 3.16 us: 1.11x slower                                               |
| sympy_sum                  | 169 ms                                                 | 192 ms: 1.13x slower                                                |
| mdp                        | 2.63 sec                                               | 2.99 sec: 1.14x slower                                              |
| xml_etree_process          | 61.7 ms                                                | 70.4 ms: 1.14x slower                                               |
| sympy_str                  | 300 ms                                                 | 349 ms: 1.16x slower                                                |
| sqlglot_transpile          | 1.68 ms                                                | 1.97 ms: 1.17x slower                                               |
| regex_v8                   | 23.1 ms                                                | 27.2 ms: 1.18x slower                                               |
| sympy_expand               | 478 ms                                                 | 562 ms: 1.18x slower                                                |
| pycparser                  | 1.18 sec                                               | 1.39 sec: 1.18x slower                                              |
| xml_etree_generate         | 89.2 ms                                                | 105 ms: 1.18x slower                                                |
| docutils                   | 2.77 sec                                               | 3.28 sec: 1.19x slower                                              |
| sympy_integrate            | 21.4 ms                                                | 25.5 ms: 1.19x slower                                               |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.19x slower                                               |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                               |
| raytrace                   | 312 ms                                                 | 374 ms: 1.20x slower                                                |
| 2to3                       | 274 ms                                                 | 332 ms: 1.21x slower                                                |
| sqlglot_normalize          | 110 ms                                                 | 134 ms: 1.21x slower                                                |
| deepcopy_memo              | 40.7 us                                                | 50.5 us: 1.24x slower                                               |
| django_template            | 34.6 ms                                                | 42.9 ms: 1.24x slower                                               |
| xml_etree_iterparse        | 107 ms                                                 | 133 ms: 1.25x slower                                                |
| meteor_contest             | 112 ms                                                 | 144 ms: 1.28x slower                                                |
| sqlglot_optimize           | 54.8 ms                                                | 71.1 ms: 1.30x slower                                               |
| deltablue                  | 3.72 ms                                                | 4.94 ms: 1.33x slower                                               |
| scimark_sor                | 129 ms                                                 | 174 ms: 1.34x slower                                                |
| coverage                   | 72.7 ms                                                | 99.3 ms: 1.37x slower                                               |
| telco                      | 7.10 ms                                                | 9.71 ms: 1.37x slower                                               |
| tomli_loads                | 2.33 sec                                               | 3.41 sec: 1.46x slower                                              |
| regex_compile              | 148 ms                                                 | 223 ms: 1.50x slower                                                |
| chaos                      | 67.0 ms                                                | 101 ms: 1.51x slower                                                |
| crypto_pyaes               | 81.9 ms                                                | 127 ms: 1.56x slower                                                |
| richards_super             | 51.5 ms                                                | 81.1 ms: 1.57x slower                                               |
| pprint_safe_repr           | 776 ms                                                 | 1.24 sec: 1.60x slower                                              |
| go                         | 139 ms                                                 | 226 ms: 1.62x slower                                                |
| comprehensions             | 21.8 us                                                | 35.2 us: 1.62x slower                                               |
| richards                   | 45.8 ms                                                | 74.5 ms: 1.62x slower                                               |
| float                      | 84.7 ms                                                | 139 ms: 1.64x slower                                                |
| pprint_pformat             | 1.57 sec                                               | 2.59 sec: 1.65x slower                                              |
| scimark_fft                | 382 ms                                                 | 630 ms: 1.65x slower                                                |
| mako                       | 11.9 ms                                                | 20.9 ms: 1.76x slower                                               |
| scimark_lu                 | 118 ms                                                 | 208 ms: 1.76x slower                                                |
| unpickle_pure_python       | 230 us                                                 | 406 us: 1.76x slower                                                |
| fannkuch                   | 417 ms                                                 | 754 ms: 1.81x slower                                                |
| nqueens                    | 83.3 ms                                                | 151 ms: 1.81x slower                                                |
| pyflate                    | 482 ms                                                 | 880 ms: 1.82x slower                                                |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 9.27 ms: 1.83x slower                                               |
| scimark_monte_carlo        | 75.1 ms                                                | 138 ms: 1.84x slower                                                |
| spectral_norm              | 115 ms                                                 | 237 ms: 2.06x slower                                                |
| nbody                      | 97.0 ms                                                | 203 ms: 2.10x slower                                                |
| hexiom                     | 6.41 ms                                                | 15.1 ms: 2.36x slower                                               |
| Geometric mean             | (ref)                                                  | 1.20x slower                                                        |

Benchmark hidden because not significant (2): bench_mp_pool, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240417-3.13.0a6+-5e20f0f-PYTHON_UOPS/bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 0.97x
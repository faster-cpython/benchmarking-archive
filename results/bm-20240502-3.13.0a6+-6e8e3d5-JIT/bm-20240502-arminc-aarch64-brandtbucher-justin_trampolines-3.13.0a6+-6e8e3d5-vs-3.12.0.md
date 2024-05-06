# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_trampolines
- machine: linux-aarch64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 308 ms                                                                | 351 ms: 1.14x slower                                                         |
| chameleon      | 8.81 ms                                                               | 9.40 ms: 1.07x slower                                                        |
| docutils       | 2.98 sec                                                              | 3.43 sec: 1.15x slower                                                       |
| html5lib       | 65.1 ms                                                               | 71.0 ms: 1.09x slower                                                        |
| tornado_http   | 136 ms                                                                | 139 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                 | 1.09x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 510 ms: 1.22x faster                                                         |
| async_tree_none_tg         | 577 ms                                                                | 473 ms: 1.22x faster                                                         |
| async_tree_memoization_tg  | 740 ms                                                                | 609 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 1.40 sec                                                              | 1.19 sec: 1.18x faster                                                       |
| async_tree_memoization     | 777 ms                                                                | 660 ms: 1.18x faster                                                         |
| async_tree_io              | 1.41 sec                                                              | 1.22 sec: 1.16x faster                                                       |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 775 ms: 1.14x faster                                                         |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 807 ms: 1.13x faster                                                         |
| Geometric mean             | (ref)                                                                 | 1.18x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 92.1 ms                                                               | 88.5 ms: 1.04x faster                                                        |
| pidigits       | 233 ms                                                                | 233 ms: 1.00x slower                                                         |
| nbody          | 105 ms                                                                | 106 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 254 ms                                                                | 254 ms: 1.00x faster                                                         |
| regex_effbot   | 4.64 ms                                                               | 4.91 ms: 1.06x slower                                                        |
| regex_v8       | 28.3 ms                                                               | 30.3 ms: 1.07x slower                                                        |
| regex_compile  | 137 ms                                                                | 163 ms: 1.19x slower                                                         |
| Geometric mean | (ref)                                                                 | 1.08x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 195 ms                                                                | 188 ms: 1.04x faster                                                         |
| xml_etree_iterparse  | 150 ms                                                                | 147 ms: 1.02x faster                                                         |
| pickle_pure_python   | 365 us                                                                | 361 us: 1.01x faster                                                         |
| tomli_loads          | 2.59 sec                                                              | 2.57 sec: 1.01x faster                                                       |
| pickle_dict          | 37.3 us                                                               | 37.7 us: 1.01x slower                                                        |
| pickle               | 13.4 us                                                               | 13.6 us: 1.01x slower                                                        |
| xml_etree_process    | 79.0 ms                                                               | 80.0 ms: 1.01x slower                                                        |
| xml_etree_generate   | 112 ms                                                                | 114 ms: 1.02x slower                                                         |
| pickle_list          | 5.25 us                                                               | 5.34 us: 1.02x slower                                                        |
| unpickle_list        | 6.17 us                                                               | 6.41 us: 1.04x slower                                                        |
| json_loads           | 30.7 us                                                               | 31.9 us: 1.04x slower                                                        |
| unpickle             | 18.5 us                                                               | 19.6 us: 1.06x slower                                                        |
| json_dumps           | 12.3 ms                                                               | 13.1 ms: 1.07x slower                                                        |
| unpickle_pure_python | 260 us                                                                | 279 us: 1.07x slower                                                         |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.37 ms                                                               | 10.7 ms: 1.28x slower                                                        |
| python_startup         | 11.4 ms                                                               | 14.7 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                                 | 1.28x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 12.9 ms                                                               | 12.8 ms: 1.01x faster                                                        |
| django_template | 40.7 ms                                                               | 50.6 ms: 1.24x slower                                                        |
| genshi_text     | 27.4 ms                                                               | 34.5 ms: 1.26x slower                                                        |
| genshi_xml      | 60.6 ms                                                               | 80.3 ms: 1.33x slower                                                        |
| Geometric mean  | (ref)                                                                 | 1.20x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 510 ms: 1.22x faster                                                         |
| async_tree_none_tg         | 577 ms                                                                | 473 ms: 1.22x faster                                                         |
| async_tree_memoization_tg  | 740 ms                                                                | 609 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 1.40 sec                                                              | 1.19 sec: 1.18x faster                                                       |
| async_tree_memoization     | 777 ms                                                                | 660 ms: 1.18x faster                                                         |
| async_tree_io              | 1.41 sec                                                              | 1.22 sec: 1.16x faster                                                       |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 775 ms: 1.14x faster                                                         |
| generators                 | 43.5 ms                                                               | 38.2 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 807 ms: 1.13x faster                                                         |
| raytrace                   | 353 ms                                                                | 317 ms: 1.11x faster                                                         |
| comprehensions             | 25.4 us                                                               | 23.6 us: 1.07x faster                                                        |
| pathlib                    | 24.5 ms                                                               | 22.9 ms: 1.07x faster                                                        |
| float                      | 92.1 ms                                                               | 88.5 ms: 1.04x faster                                                        |
| xml_etree_parse            | 195 ms                                                                | 188 ms: 1.04x faster                                                         |
| xml_etree_iterparse        | 150 ms                                                                | 147 ms: 1.02x faster                                                         |
| logging_format             | 8.34 us                                                               | 8.19 us: 1.02x faster                                                        |
| pickle_pure_python         | 365 us                                                                | 361 us: 1.01x faster                                                         |
| logging_simple             | 7.63 us                                                               | 7.55 us: 1.01x faster                                                        |
| mako                       | 12.9 ms                                                               | 12.8 ms: 1.01x faster                                                        |
| tomli_loads                | 2.59 sec                                                              | 2.57 sec: 1.01x faster                                                       |
| regex_dna                  | 254 ms                                                                | 254 ms: 1.00x faster                                                         |
| pidigits                   | 233 ms                                                                | 233 ms: 1.00x slower                                                         |
| pickle_dict                | 37.3 us                                                               | 37.7 us: 1.01x slower                                                        |
| pickle                     | 13.4 us                                                               | 13.6 us: 1.01x slower                                                        |
| xml_etree_process          | 79.0 ms                                                               | 80.0 ms: 1.01x slower                                                        |
| nbody                      | 105 ms                                                                | 106 ms: 1.01x slower                                                         |
| xml_etree_generate         | 112 ms                                                                | 114 ms: 1.02x slower                                                         |
| crypto_pyaes               | 86.6 ms                                                               | 88.1 ms: 1.02x slower                                                        |
| sqlite_synth               | 3.77 us                                                               | 3.84 us: 1.02x slower                                                        |
| pickle_list                | 5.25 us                                                               | 5.34 us: 1.02x slower                                                        |
| bench_thread_pool          | 1.31 ms                                                               | 1.33 ms: 1.02x slower                                                        |
| deepcopy_reduce            | 4.10 us                                                               | 4.19 us: 1.02x slower                                                        |
| tornado_http               | 136 ms                                                                | 139 ms: 1.02x slower                                                         |
| asyncio_tcp_ssl            | 2.19 sec                                                              | 2.24 sec: 1.03x slower                                                       |
| deepcopy_memo              | 49.6 us                                                               | 50.9 us: 1.03x slower                                                        |
| json                       | 5.54 ms                                                               | 5.68 ms: 1.03x slower                                                        |
| fannkuch                   | 443 ms                                                                | 456 ms: 1.03x slower                                                         |
| sqlglot_parse              | 1.46 ms                                                               | 1.51 ms: 1.03x slower                                                        |
| richards_super             | 58.5 ms                                                               | 60.2 ms: 1.03x slower                                                        |
| async_generators           | 491 ms                                                                | 506 ms: 1.03x slower                                                         |
| pycparser                  | 1.26 sec                                                              | 1.30 sec: 1.03x slower                                                       |
| thrift                     | 937 us                                                                | 968 us: 1.03x slower                                                         |
| sqlglot_transpile          | 1.83 ms                                                               | 1.89 ms: 1.03x slower                                                        |
| coroutines                 | 29.0 ms                                                               | 30.1 ms: 1.04x slower                                                        |
| unpickle_list              | 6.17 us                                                               | 6.41 us: 1.04x slower                                                        |
| deepcopy                   | 446 us                                                                | 463 us: 1.04x slower                                                         |
| json_loads                 | 30.7 us                                                               | 31.9 us: 1.04x slower                                                        |
| richards                   | 50.9 ms                                                               | 53.3 ms: 1.05x slower                                                        |
| logging_silent             | 127 ns                                                                | 133 ns: 1.05x slower                                                         |
| regex_effbot               | 4.64 ms                                                               | 4.91 ms: 1.06x slower                                                        |
| unpickle                   | 18.5 us                                                               | 19.6 us: 1.06x slower                                                        |
| dask                       | 376 ms                                                                | 401 ms: 1.07x slower                                                         |
| spectral_norm              | 131 ms                                                                | 139 ms: 1.07x slower                                                         |
| chameleon                  | 8.81 ms                                                               | 9.40 ms: 1.07x slower                                                        |
| regex_v8                   | 28.3 ms                                                               | 30.3 ms: 1.07x slower                                                        |
| json_dumps                 | 12.3 ms                                                               | 13.1 ms: 1.07x slower                                                        |
| meteor_contest             | 112 ms                                                                | 120 ms: 1.07x slower                                                         |
| unpickle_pure_python       | 260 us                                                                | 279 us: 1.07x slower                                                         |
| scimark_fft                | 418 ms                                                                | 449 ms: 1.07x slower                                                         |
| pyflate                    | 559 ms                                                                | 600 ms: 1.07x slower                                                         |
| html5lib                   | 65.1 ms                                                               | 71.0 ms: 1.09x slower                                                        |
| asyncio_tcp                | 566 ms                                                                | 621 ms: 1.10x slower                                                         |
| sqlglot_normalize          | 126 ms                                                                | 139 ms: 1.10x slower                                                         |
| sympy_str                  | 280 ms                                                                | 310 ms: 1.11x slower                                                         |
| scimark_sparse_mat_mult    | 6.19 ms                                                               | 6.90 ms: 1.11x slower                                                        |
| bench_mp_pool              | 7.05 ms                                                               | 7.91 ms: 1.12x slower                                                        |
| deltablue                  | 4.12 ms                                                               | 4.62 ms: 1.12x slower                                                        |
| sqlglot_optimize           | 61.3 ms                                                               | 68.9 ms: 1.12x slower                                                        |
| gc_traversal               | 4.40 ms                                                               | 4.96 ms: 1.13x slower                                                        |
| telco                      | 8.51 ms                                                               | 9.69 ms: 1.14x slower                                                        |
| 2to3                       | 308 ms                                                                | 351 ms: 1.14x slower                                                         |
| coverage                   | 87.3 ms                                                               | 100 ms: 1.15x slower                                                         |
| dulwich_log                | 62.0 ms                                                               | 71.3 ms: 1.15x slower                                                        |
| docutils                   | 2.98 sec                                                              | 3.43 sec: 1.15x slower                                                       |
| sympy_sum                  | 154 ms                                                                | 179 ms: 1.16x slower                                                         |
| sympy_expand               | 454 ms                                                                | 527 ms: 1.16x slower                                                         |
| pylint                     | 355 ms                                                                | 413 ms: 1.16x slower                                                         |
| typing_runtime_protocols   | 181 us                                                                | 211 us: 1.17x slower                                                         |
| go                         | 157 ms                                                                | 185 ms: 1.18x slower                                                         |
| regex_compile              | 137 ms                                                                | 163 ms: 1.19x slower                                                         |
| sympy_integrate            | 21.6 ms                                                               | 25.9 ms: 1.20x slower                                                        |
| create_gc_cycles           | 1.92 ms                                                               | 2.30 ms: 1.20x slower                                                        |
| chaos                      | 71.4 ms                                                               | 85.7 ms: 1.20x slower                                                        |
| nqueens                    | 99.2 ms                                                               | 120 ms: 1.21x slower                                                         |
| scimark_sor                | 150 ms                                                                | 184 ms: 1.23x slower                                                         |
| scimark_lu                 | 146 ms                                                                | 180 ms: 1.24x slower                                                         |
| django_template            | 40.7 ms                                                               | 50.6 ms: 1.24x slower                                                        |
| genshi_text                | 27.4 ms                                                               | 34.5 ms: 1.26x slower                                                        |
| pprint_safe_repr           | 916 ms                                                                | 1.17 sec: 1.27x slower                                                       |
| python_startup_no_site     | 8.37 ms                                                               | 10.7 ms: 1.28x slower                                                        |
| hexiom                     | 6.98 ms                                                               | 8.97 ms: 1.29x slower                                                        |
| pprint_pformat             | 1.88 sec                                                              | 2.42 sec: 1.29x slower                                                       |
| python_startup             | 11.4 ms                                                               | 14.7 ms: 1.29x slower                                                        |
| genshi_xml                 | 60.6 ms                                                               | 80.3 ms: 1.33x slower                                                        |
| Geometric mean             | (ref)                                                                 | 1.06x slower                                                                 |

Benchmark hidden because not significant (3): scimark_monte_carlo, asyncio_websockets, mdp
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 0.99x
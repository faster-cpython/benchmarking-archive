# Results vs. base

- fork: brandtbucher
- ref: justin_trampolines
- machine: linux-aarch64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.00x slower
- HPT reliability: 97.28%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                                   | 351 ms: 1.01x slower                                                         |
| chameleon      | 9.37 ms                                                                  | 9.40 ms: 1.00x slower                                                        |
| docutils       | 3.40 sec                                                                 | 3.43 sec: 1.01x slower                                                       |
| html5lib       | 70.4 ms                                                                  | 71.0 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_none_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 107 ms                                                                   | 106 ms: 1.01x faster                                                         |
| float          | 89.2 ms                                                                  | 88.5 ms: 1.01x faster                                                        |
| pidigits       | 233 ms                                                                   | 233 ms: 1.00x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 30.2 ms                                                                  | 30.3 ms: 1.00x slower                                                        |
| regex_effbot   | 4.85 ms                                                                  | 4.91 ms: 1.01x slower                                                        |
| regex_compile  | 160 ms                                                                   | 163 ms: 1.02x slower                                                         |
| regex_dna      | 247 ms                                                                   | 254 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 19.7 us                                                                  | 19.6 us: 1.01x faster                                                        |
| xml_etree_process    | 80.3 ms                                                                  | 80.0 ms: 1.00x faster                                                        |
| pickle_dict          | 37.8 us                                                                  | 37.7 us: 1.00x faster                                                        |
| xml_etree_generate   | 113 ms                                                                   | 114 ms: 1.01x slower                                                         |
| unpickle_pure_python | 276 us                                                                   | 279 us: 1.01x slower                                                         |
| pickle               | 13.4 us                                                                  | 13.6 us: 1.01x slower                                                        |
| unpickle_list        | 6.31 us                                                                  | 6.41 us: 1.02x slower                                                        |
| pickle_pure_python   | 354 us                                                                   | 361 us: 1.02x slower                                                         |
| pickle_list          | 5.23 us                                                                  | 5.34 us: 1.02x slower                                                        |
| json_dumps           | 12.8 ms                                                                  | 13.1 ms: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (4): tomli_loads, xml_etree_iterparse, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 79.5 ms                                                                  | 80.3 ms: 1.01x slower                                                        |
| genshi_text     | 33.8 ms                                                                  | 34.5 ms: 1.02x slower                                                        |
| django_template | 48.3 ms                                                                  | 50.6 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|--------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| bench_mp_pool            | 8.69 ms                                                                  | 7.91 ms: 1.10x faster                                                        |
| telco                    | 10.3 ms                                                                  | 9.69 ms: 1.06x faster                                                        |
| spectral_norm            | 143 ms                                                                   | 139 ms: 1.02x faster                                                         |
| pathlib                  | 23.3 ms                                                                  | 22.9 ms: 1.02x faster                                                        |
| gc_traversal             | 5.05 ms                                                                  | 4.96 ms: 1.02x faster                                                        |
| logging_format           | 8.34 us                                                                  | 8.19 us: 1.02x faster                                                        |
| thrift                   | 985 us                                                                   | 968 us: 1.02x faster                                                         |
| asyncio_tcp_ssl          | 2.27 sec                                                                 | 2.24 sec: 1.01x faster                                                       |
| nbody                    | 107 ms                                                                   | 106 ms: 1.01x faster                                                         |
| fannkuch                 | 461 ms                                                                   | 456 ms: 1.01x faster                                                         |
| pprint_safe_repr         | 1.18 sec                                                                 | 1.17 sec: 1.01x faster                                                       |
| go                       | 187 ms                                                                   | 185 ms: 1.01x faster                                                         |
| scimark_fft              | 453 ms                                                                   | 449 ms: 1.01x faster                                                         |
| typing_runtime_protocols | 213 us                                                                   | 211 us: 1.01x faster                                                         |
| logging_simple           | 7.61 us                                                                  | 7.55 us: 1.01x faster                                                        |
| async_generators         | 510 ms                                                                   | 506 ms: 1.01x faster                                                         |
| deepcopy_reduce          | 4.22 us                                                                  | 4.19 us: 1.01x faster                                                        |
| float                    | 89.2 ms                                                                  | 88.5 ms: 1.01x faster                                                        |
| unpickle                 | 19.7 us                                                                  | 19.6 us: 1.01x faster                                                        |
| scimark_lu               | 181 ms                                                                   | 180 ms: 1.01x faster                                                         |
| xml_etree_process        | 80.3 ms                                                                  | 80.0 ms: 1.00x faster                                                        |
| pickle_dict              | 37.8 us                                                                  | 37.7 us: 1.00x faster                                                        |
| pidigits                 | 233 ms                                                                   | 233 ms: 1.00x slower                                                         |
| regex_v8                 | 30.2 ms                                                                  | 30.3 ms: 1.00x slower                                                        |
| chameleon                | 9.37 ms                                                                  | 9.40 ms: 1.00x slower                                                        |
| generators               | 38.1 ms                                                                  | 38.2 ms: 1.00x slower                                                        |
| deepcopy                 | 461 us                                                                   | 463 us: 1.00x slower                                                         |
| xml_etree_generate       | 113 ms                                                                   | 114 ms: 1.01x slower                                                         |
| coroutines               | 29.9 ms                                                                  | 30.1 ms: 1.01x slower                                                        |
| sqlite_synth             | 3.81 us                                                                  | 3.84 us: 1.01x slower                                                        |
| comprehensions           | 23.5 us                                                                  | 23.6 us: 1.01x slower                                                        |
| crypto_pyaes             | 87.5 ms                                                                  | 88.1 ms: 1.01x slower                                                        |
| scimark_sor              | 183 ms                                                                   | 184 ms: 1.01x slower                                                         |
| sympy_str                | 307 ms                                                                   | 310 ms: 1.01x slower                                                         |
| 2to3                     | 348 ms                                                                   | 351 ms: 1.01x slower                                                         |
| scimark_monte_carlo      | 84.4 ms                                                                  | 85.1 ms: 1.01x slower                                                        |
| html5lib                 | 70.4 ms                                                                  | 71.0 ms: 1.01x slower                                                        |
| unpickle_pure_python     | 276 us                                                                   | 279 us: 1.01x slower                                                         |
| coverage                 | 99.2 ms                                                                  | 100 ms: 1.01x slower                                                         |
| pickle                   | 13.4 us                                                                  | 13.6 us: 1.01x slower                                                        |
| genshi_xml               | 79.5 ms                                                                  | 80.3 ms: 1.01x slower                                                        |
| pycparser                | 1.28 sec                                                                 | 1.30 sec: 1.01x slower                                                       |
| meteor_contest           | 119 ms                                                                   | 120 ms: 1.01x slower                                                         |
| docutils                 | 3.40 sec                                                                 | 3.43 sec: 1.01x slower                                                       |
| sympy_expand             | 520 ms                                                                   | 527 ms: 1.01x slower                                                         |
| sqlglot_optimize         | 68.0 ms                                                                  | 68.9 ms: 1.01x slower                                                        |
| regex_effbot             | 4.85 ms                                                                  | 4.91 ms: 1.01x slower                                                        |
| sympy_integrate          | 25.5 ms                                                                  | 25.9 ms: 1.01x slower                                                        |
| pyflate                  | 592 ms                                                                   | 600 ms: 1.01x slower                                                         |
| sqlglot_normalize        | 137 ms                                                                   | 139 ms: 1.01x slower                                                         |
| richards_super           | 59.3 ms                                                                  | 60.2 ms: 1.01x slower                                                        |
| unpickle_list            | 6.31 us                                                                  | 6.41 us: 1.02x slower                                                        |
| richards                 | 52.5 ms                                                                  | 53.3 ms: 1.02x slower                                                        |
| regex_compile            | 160 ms                                                                   | 163 ms: 1.02x slower                                                         |
| pickle_pure_python       | 354 us                                                                   | 361 us: 1.02x slower                                                         |
| pickle_list              | 5.23 us                                                                  | 5.34 us: 1.02x slower                                                        |
| genshi_text              | 33.8 ms                                                                  | 34.5 ms: 1.02x slower                                                        |
| json_dumps               | 12.8 ms                                                                  | 13.1 ms: 1.02x slower                                                        |
| sympy_sum                | 174 ms                                                                   | 179 ms: 1.02x slower                                                         |
| regex_dna                | 247 ms                                                                   | 254 ms: 1.03x slower                                                         |
| chaos                    | 82.1 ms                                                                  | 85.7 ms: 1.04x slower                                                        |
| django_template          | 48.3 ms                                                                  | 50.6 ms: 1.05x slower                                                        |
| Geometric mean           | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (35): async_tree_io, scimark_sparse_mat_mult, tornado_http, async_tree_memoization_tg, async_tree_io_tg, create_gc_cycles, asyncio_tcp, pprint_pformat, nqueens, sqlglot_parse, mako, tomli_loads, xml_etree_iterparse, python_startup_no_site, raytrace, logging_silent, mdp, json_loads, asyncio_websockets, async_tree_memoization, xml_etree_parse, async_tree_cpu_io_mixed_tg, sqlglot_transpile, async_tree_none, hexiom, deepcopy_memo, python_startup, async_tree_none_tg, async_tree_cpu_io_mixed, json, bench_thread_pool, deltablue, dulwich_log, pylint, dask

# HPT report

- Reliability score: 97.28% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache_1
- machine: linux-x86_64
- commit hash: b8620f7
- commit date: 2024-04-23
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 277 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (4): chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_io_tg, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 81.0 ms: 1.12x faster                                                        |
| float          | 77.2 ms                                                                | 73.7 ms: 1.05x faster                                                        |
| pidigits       | 189 ms                                                                 | 189 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                                 | 140 ms: 1.01x faster                                                         |
| regex_v8       | 25.2 ms                                                                | 25.0 ms: 1.01x faster                                                        |
| regex_dna      | 230 ms                                                                 | 229 ms: 1.00x faster                                                         |
| regex_effbot   | 3.67 ms                                                                | 4.21 ms: 1.14x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 237 us                                                                 | 223 us: 1.06x faster                                                         |
| tomli_loads          | 2.03 sec                                                               | 1.92 sec: 1.06x faster                                                       |
| xml_etree_iterparse  | 104 ms                                                                 | 101 ms: 1.03x faster                                                         |
| xml_etree_parse      | 152 ms                                                                 | 148 ms: 1.02x faster                                                         |
| pickle_list          | 5.11 us                                                                | 5.06 us: 1.01x faster                                                        |
| pickle_pure_python   | 308 us                                                                 | 309 us: 1.00x slower                                                         |
| xml_etree_generate   | 87.3 ms                                                                | 87.6 ms: 1.00x slower                                                        |
| unpickle_list        | 5.16 us                                                                | 5.20 us: 1.01x slower                                                        |
| xml_etree_process    | 60.1 ms                                                                | 60.6 ms: 1.01x slower                                                        |
| pickle               | 11.6 us                                                                | 11.8 us: 1.02x slower                                                        |
| pickle_dict          | 34.0 us                                                                | 35.6 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (3): unpickle, json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| python_startup_no_site | 7.57 ms                                                                | 7.68 ms: 1.02x slower                                                        |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 9.91 ms: 1.09x faster                                                        |
| django_template | 36.4 ms                                                                | 35.8 ms: 1.02x faster                                                        |
| genshi_text     | 24.5 ms                                                                | 24.1 ms: 1.01x faster                                                        |
| genshi_xml      | 53.7 ms                                                                | 55.9 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| spectral_norm            | 114 ms                                                                 | 98.5 ms: 1.15x faster                                                        |
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.42 ms: 1.12x faster                                                        |
| nbody                    | 90.4 ms                                                                | 81.0 ms: 1.12x faster                                                        |
| scimark_fft              | 344 ms                                                                 | 310 ms: 1.11x faster                                                         |
| scimark_monte_carlo      | 70.0 ms                                                                | 63.6 ms: 1.10x faster                                                        |
| mako                     | 10.8 ms                                                                | 9.91 ms: 1.09x faster                                                        |
| logging_silent           | 108 ns                                                                 | 99.0 ns: 1.09x faster                                                        |
| fannkuch                 | 386 ms                                                                 | 356 ms: 1.08x faster                                                         |
| gc_traversal             | 4.01 ms                                                                | 3.74 ms: 1.07x faster                                                        |
| pprint_safe_repr         | 763 ms                                                                 | 717 ms: 1.06x faster                                                         |
| crypto_pyaes             | 73.3 ms                                                                | 68.9 ms: 1.06x faster                                                        |
| unpickle_pure_python     | 237 us                                                                 | 223 us: 1.06x faster                                                         |
| tomli_loads              | 2.03 sec                                                               | 1.92 sec: 1.06x faster                                                       |
| hexiom                   | 6.88 ms                                                                | 6.54 ms: 1.05x faster                                                        |
| scimark_lu               | 132 ms                                                                 | 125 ms: 1.05x faster                                                         |
| go                       | 155 ms                                                                 | 148 ms: 1.05x faster                                                         |
| pprint_pformat           | 1.55 sec                                                               | 1.48 sec: 1.05x faster                                                       |
| float                    | 77.2 ms                                                                | 73.7 ms: 1.05x faster                                                        |
| comprehensions           | 17.7 us                                                                | 16.9 us: 1.05x faster                                                        |
| scimark_sor              | 134 ms                                                                 | 129 ms: 1.04x faster                                                         |
| pyflate                  | 463 ms                                                                 | 443 ms: 1.04x faster                                                         |
| nqueens                  | 89.8 ms                                                                | 86.7 ms: 1.04x faster                                                        |
| richards                 | 43.7 ms                                                                | 42.4 ms: 1.03x faster                                                        |
| xml_etree_iterparse      | 104 ms                                                                 | 101 ms: 1.03x faster                                                         |
| chaos                    | 63.4 ms                                                                | 61.8 ms: 1.03x faster                                                        |
| deltablue                | 3.73 ms                                                                | 3.64 ms: 1.02x faster                                                        |
| meteor_contest           | 111 ms                                                                 | 108 ms: 1.02x faster                                                         |
| xml_etree_parse          | 152 ms                                                                 | 148 ms: 1.02x faster                                                         |
| telco                    | 8.73 ms                                                                | 8.56 ms: 1.02x faster                                                        |
| pycparser                | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                       |
| django_template          | 36.4 ms                                                                | 35.8 ms: 1.02x faster                                                        |
| mdp                      | 2.68 sec                                                               | 2.64 sec: 1.02x faster                                                       |
| typing_runtime_protocols | 117 us                                                                 | 115 us: 1.02x faster                                                         |
| genshi_text              | 24.5 ms                                                                | 24.1 ms: 1.01x faster                                                        |
| sqlglot_transpile        | 1.65 ms                                                                | 1.63 ms: 1.01x faster                                                        |
| generators               | 30.3 ms                                                                | 29.9 ms: 1.01x faster                                                        |
| pickle_list              | 5.11 us                                                                | 5.06 us: 1.01x faster                                                        |
| regex_compile            | 141 ms                                                                 | 140 ms: 1.01x faster                                                         |
| logging_simple           | 5.81 us                                                                | 5.76 us: 1.01x faster                                                        |
| sqlglot_parse            | 1.32 ms                                                                | 1.31 ms: 1.01x faster                                                        |
| regex_v8                 | 25.2 ms                                                                | 25.0 ms: 1.01x faster                                                        |
| logging_format           | 6.47 us                                                                | 6.41 us: 1.01x faster                                                        |
| sympy_integrate          | 22.0 ms                                                                | 21.9 ms: 1.01x faster                                                        |
| sympy_str                | 295 ms                                                                 | 293 ms: 1.01x faster                                                         |
| sympy_sum                | 168 ms                                                                 | 167 ms: 1.01x faster                                                         |
| asyncio_websockets       | 566 ms                                                                 | 563 ms: 1.01x faster                                                         |
| regex_dna                | 230 ms                                                                 | 229 ms: 1.00x faster                                                         |
| pidigits                 | 189 ms                                                                 | 189 ms: 1.00x faster                                                         |
| 2to3                     | 277 ms                                                                 | 277 ms: 1.00x faster                                                         |
| pickle_pure_python       | 308 us                                                                 | 309 us: 1.00x slower                                                         |
| xml_etree_generate       | 87.3 ms                                                                | 87.6 ms: 1.00x slower                                                        |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                       |
| create_gc_cycles         | 1.77 ms                                                                | 1.77 ms: 1.00x slower                                                        |
| thrift                   | 823 us                                                                 | 827 us: 1.00x slower                                                         |
| bench_thread_pool        | 859 us                                                                 | 864 us: 1.01x slower                                                         |
| sqlglot_normalize        | 113 ms                                                                 | 114 ms: 1.01x slower                                                         |
| unpickle_list            | 5.16 us                                                                | 5.20 us: 1.01x slower                                                        |
| deepcopy                 | 361 us                                                                 | 364 us: 1.01x slower                                                         |
| xml_etree_process        | 60.1 ms                                                                | 60.6 ms: 1.01x slower                                                        |
| pathlib                  | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                        |
| async_generators         | 462 ms                                                                 | 467 ms: 1.01x slower                                                         |
| asyncio_tcp              | 509 ms                                                                 | 515 ms: 1.01x slower                                                         |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| coverage                 | 96.7 ms                                                                | 98.1 ms: 1.01x slower                                                        |
| python_startup_no_site   | 7.57 ms                                                                | 7.68 ms: 1.02x slower                                                        |
| pickle                   | 11.6 us                                                                | 11.8 us: 1.02x slower                                                        |
| genshi_xml               | 53.7 ms                                                                | 55.9 ms: 1.04x slower                                                        |
| pickle_dict              | 34.0 us                                                                | 35.6 us: 1.05x slower                                                        |
| regex_effbot             | 3.67 ms                                                                | 4.21 ms: 1.14x slower                                                        |
| Geometric mean           | (ref)                                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (32): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none_tg, unpickle, dask, async_tree_memoization_tg, async_tree_none, richards_super, async_tree_io_tg, pylint, json, sqlite_synth, dulwich_log, deepcopy_reduce, deepcopy_memo, sqlglot_optimize, tornado_http, async_tree_memoization, docutils, sympy_expand, coroutines, html5lib, raytrace, json_loads, mypy2, bench_mp_pool, chameleon, gunicorn, aiohttp, json_dumps, async_tree_io, djangocms

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
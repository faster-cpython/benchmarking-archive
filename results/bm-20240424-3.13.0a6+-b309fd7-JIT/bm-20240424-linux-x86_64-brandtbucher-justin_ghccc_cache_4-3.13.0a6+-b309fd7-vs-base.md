# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache_4
- machine: linux-x86_64
- commit hash: b309fd7
- commit date: 2024-04-24
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 290 ms: 1.04x slower                                                         |
| chameleon      | 7.11 ms                                                                | 7.24 ms: 1.02x slower                                                        |
| docutils       | 2.91 sec                                                               | 3.00 sec: 1.03x slower                                                       |
| html5lib       | 68.8 ms                                                                | 70.0 ms: 1.02x slower                                                        |
| tornado_http   | 95.9 ms                                                                | 98.0 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 83.1 ms: 1.09x faster                                                        |
| float          | 77.2 ms                                                                | 75.3 ms: 1.02x faster                                                        |
| pidigits       | 189 ms                                                                 | 210 ms: 1.11x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 25.2 ms                                                                | 24.5 ms: 1.03x faster                                                        |
| regex_dna      | 230 ms                                                                 | 225 ms: 1.02x faster                                                         |
| regex_effbot   | 3.67 ms                                                                | 4.23 ms: 1.15x slower                                                        |
| regex_compile  | 141 ms                                                                 | 171 ms: 1.21x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 152 ms                                                                 | 148 ms: 1.02x faster                                                         |
| unpickle             | 15.5 us                                                                | 15.2 us: 1.02x faster                                                        |
| pickle_list          | 5.11 us                                                                | 5.08 us: 1.01x faster                                                        |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                        |
| xml_etree_iterparse  | 104 ms                                                                 | 104 ms: 1.00x faster                                                         |
| pickle_pure_python   | 308 us                                                                 | 309 us: 1.00x slower                                                         |
| xml_etree_generate   | 87.3 ms                                                                | 88.1 ms: 1.01x slower                                                        |
| xml_etree_process    | 60.1 ms                                                                | 60.9 ms: 1.01x slower                                                        |
| unpickle_pure_python | 237 us                                                                 | 240 us: 1.01x slower                                                         |
| pickle_dict          | 34.0 us                                                                | 34.9 us: 1.03x slower                                                        |
| unpickle_list        | 5.16 us                                                                | 5.34 us: 1.04x slower                                                        |
| pickle               | 11.6 us                                                                | 12.0 us: 1.04x slower                                                        |
| tomli_loads          | 2.03 sec                                                               | 2.15 sec: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| python_startup_no_site | 7.57 ms                                                                | 7.71 ms: 1.02x slower                                                        |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.7 ms: 1.01x faster                                                        |
| genshi_text     | 24.5 ms                                                                | 25.2 ms: 1.03x slower                                                        |
| django_template | 36.4 ms                                                                | 37.5 ms: 1.03x slower                                                        |
| genshi_xml      | 53.7 ms                                                                | 61.1 ms: 1.14x slower                                                        |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.55 ms: 1.09x faster                                                        |
| nbody                    | 90.4 ms                                                                | 83.1 ms: 1.09x faster                                                        |
| logging_silent           | 108 ns                                                                 | 102 ns: 1.06x faster                                                         |
| spectral_norm            | 114 ms                                                                 | 108 ms: 1.05x faster                                                         |
| scimark_fft              | 344 ms                                                                 | 333 ms: 1.03x faster                                                         |
| regex_v8                 | 25.2 ms                                                                | 24.5 ms: 1.03x faster                                                        |
| float                    | 77.2 ms                                                                | 75.3 ms: 1.02x faster                                                        |
| xml_etree_parse          | 152 ms                                                                 | 148 ms: 1.02x faster                                                         |
| regex_dna                | 230 ms                                                                 | 225 ms: 1.02x faster                                                         |
| gc_traversal             | 4.01 ms                                                                | 3.93 ms: 1.02x faster                                                        |
| scimark_lu               | 132 ms                                                                 | 130 ms: 1.02x faster                                                         |
| unpickle                 | 15.5 us                                                                | 15.2 us: 1.02x faster                                                        |
| mako                     | 10.8 ms                                                                | 10.7 ms: 1.01x faster                                                        |
| typing_runtime_protocols | 117 us                                                                 | 116 us: 1.01x faster                                                         |
| scimark_sor              | 134 ms                                                                 | 133 ms: 1.01x faster                                                         |
| generators               | 30.3 ms                                                                | 30.0 ms: 1.01x faster                                                        |
| pickle_list              | 5.11 us                                                                | 5.08 us: 1.01x faster                                                        |
| json_dumps               | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                        |
| xml_etree_iterparse      | 104 ms                                                                 | 104 ms: 1.00x faster                                                         |
| asyncio_websockets       | 566 ms                                                                 | 564 ms: 1.00x faster                                                         |
| pickle_pure_python       | 308 us                                                                 | 309 us: 1.00x slower                                                         |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.87 sec: 1.00x slower                                                       |
| crypto_pyaes             | 73.3 ms                                                                | 73.7 ms: 1.00x slower                                                        |
| thrift                   | 823 us                                                                 | 829 us: 1.01x slower                                                         |
| meteor_contest           | 111 ms                                                                 | 112 ms: 1.01x slower                                                         |
| xml_etree_generate       | 87.3 ms                                                                | 88.1 ms: 1.01x slower                                                        |
| sqlite_synth             | 2.86 us                                                                | 2.89 us: 1.01x slower                                                        |
| create_gc_cycles         | 1.77 ms                                                                | 1.79 ms: 1.01x slower                                                        |
| telco                    | 8.73 ms                                                                | 8.84 ms: 1.01x slower                                                        |
| fannkuch                 | 386 ms                                                                 | 391 ms: 1.01x slower                                                         |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| xml_etree_process        | 60.1 ms                                                                | 60.9 ms: 1.01x slower                                                        |
| coroutines               | 22.6 ms                                                                | 22.9 ms: 1.01x slower                                                        |
| unpickle_pure_python     | 237 us                                                                 | 240 us: 1.01x slower                                                         |
| gunicorn                 | 1.30 ms                                                                | 1.32 ms: 1.02x slower                                                        |
| asyncio_tcp              | 509 ms                                                                 | 517 ms: 1.02x slower                                                         |
| coverage                 | 96.7 ms                                                                | 98.3 ms: 1.02x slower                                                        |
| aiohttp                  | 1.21 ms                                                                | 1.23 ms: 1.02x slower                                                        |
| bench_thread_pool        | 859 us                                                                 | 874 us: 1.02x slower                                                         |
| html5lib                 | 68.8 ms                                                                | 70.0 ms: 1.02x slower                                                        |
| python_startup_no_site   | 7.57 ms                                                                | 7.71 ms: 1.02x slower                                                        |
| pycparser                | 1.19 sec                                                               | 1.21 sec: 1.02x slower                                                       |
| chameleon                | 7.11 ms                                                                | 7.24 ms: 1.02x slower                                                        |
| async_generators         | 462 ms                                                                 | 471 ms: 1.02x slower                                                         |
| pathlib                  | 17.6 ms                                                                | 18.0 ms: 1.02x slower                                                        |
| tornado_http             | 95.9 ms                                                                | 98.0 ms: 1.02x slower                                                        |
| deepcopy_memo            | 39.2 us                                                                | 40.1 us: 1.02x slower                                                        |
| pickle_dict              | 34.0 us                                                                | 34.9 us: 1.03x slower                                                        |
| deepcopy                 | 361 us                                                                 | 372 us: 1.03x slower                                                         |
| sqlglot_transpile        | 1.65 ms                                                                | 1.70 ms: 1.03x slower                                                        |
| genshi_text              | 24.5 ms                                                                | 25.2 ms: 1.03x slower                                                        |
| django_template          | 36.4 ms                                                                | 37.5 ms: 1.03x slower                                                        |
| docutils                 | 2.91 sec                                                               | 3.00 sec: 1.03x slower                                                       |
| sqlglot_normalize        | 113 ms                                                                 | 116 ms: 1.03x slower                                                         |
| mypy2                    | 784 ms                                                                 | 809 ms: 1.03x slower                                                         |
| sympy_sum                | 168 ms                                                                 | 174 ms: 1.03x slower                                                         |
| unpickle_list            | 5.16 us                                                                | 5.34 us: 1.04x slower                                                        |
| sympy_integrate          | 22.0 ms                                                                | 22.8 ms: 1.04x slower                                                        |
| logging_format           | 6.47 us                                                                | 6.70 us: 1.04x slower                                                        |
| pickle                   | 11.6 us                                                                | 12.0 us: 1.04x slower                                                        |
| sqlglot_optimize         | 57.2 ms                                                                | 59.5 ms: 1.04x slower                                                        |
| dulwich_log              | 69.3 ms                                                                | 72.2 ms: 1.04x slower                                                        |
| 2to3                     | 277 ms                                                                 | 290 ms: 1.04x slower                                                         |
| sqlglot_parse            | 1.32 ms                                                                | 1.38 ms: 1.05x slower                                                        |
| logging_simple           | 5.81 us                                                                | 6.11 us: 1.05x slower                                                        |
| sympy_str                | 295 ms                                                                 | 310 ms: 1.05x slower                                                         |
| raytrace                 | 273 ms                                                                 | 288 ms: 1.05x slower                                                         |
| tomli_loads              | 2.03 sec                                                               | 2.15 sec: 1.06x slower                                                       |
| sympy_expand             | 494 ms                                                                 | 524 ms: 1.06x slower                                                         |
| chaos                    | 63.4 ms                                                                | 67.4 ms: 1.06x slower                                                        |
| nqueens                  | 89.8 ms                                                                | 95.5 ms: 1.06x slower                                                        |
| scimark_monte_carlo      | 70.0 ms                                                                | 74.6 ms: 1.07x slower                                                        |
| comprehensions           | 17.7 us                                                                | 19.0 us: 1.07x slower                                                        |
| richards                 | 43.7 ms                                                                | 47.7 ms: 1.09x slower                                                        |
| richards_super           | 49.4 ms                                                                | 54.3 ms: 1.10x slower                                                        |
| pyflate                  | 463 ms                                                                 | 514 ms: 1.11x slower                                                         |
| pidigits                 | 189 ms                                                                 | 210 ms: 1.11x slower                                                         |
| genshi_xml               | 53.7 ms                                                                | 61.1 ms: 1.14x slower                                                        |
| regex_effbot             | 3.67 ms                                                                | 4.23 ms: 1.15x slower                                                        |
| pprint_safe_repr         | 763 ms                                                                 | 897 ms: 1.18x slower                                                         |
| hexiom                   | 6.88 ms                                                                | 8.20 ms: 1.19x slower                                                        |
| regex_compile            | 141 ms                                                                 | 171 ms: 1.21x slower                                                         |
| pprint_pformat           | 1.55 sec                                                               | 1.94 sec: 1.25x slower                                                       |
| Geometric mean           | (ref)                                                                  | 1.03x slower                                                                 |

Benchmark hidden because not significant (18): async_tree_io_tg, async_tree_cpu_io_mixed_tg, go, mdp, async_tree_io, bench_mp_pool, deepcopy_reduce, json_loads, async_tree_cpu_io_mixed, dask, json, async_tree_none_tg, async_tree_memoization_tg, deltablue, async_tree_none, pylint, djangocms, async_tree_memoization

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.04x
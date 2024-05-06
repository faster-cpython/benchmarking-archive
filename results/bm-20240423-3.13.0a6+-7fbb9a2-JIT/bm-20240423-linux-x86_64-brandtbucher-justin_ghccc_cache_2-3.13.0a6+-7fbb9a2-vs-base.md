# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache_2
- machine: linux-x86_64
- commit hash: 7fbb9a2
- commit date: 2024-04-23
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 275 ms: 1.01x faster                                                         |
| chameleon      | 7.11 ms                                                                | 6.88 ms: 1.03x faster                                                        |
| docutils       | 2.91 sec                                                               | 2.89 sec: 1.00x faster                                                       |
| html5lib       | 68.8 ms                                                                | 68.0 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none, async_tree_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_memoization_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 77.3 ms: 1.17x faster                                                        |
| float          | 77.2 ms                                                                | 72.4 ms: 1.07x faster                                                        |
| pidigits       | 189 ms                                                                 | 189 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 230 ms                                                                 | 218 ms: 1.05x faster                                                         |
| regex_v8       | 25.2 ms                                                                | 24.7 ms: 1.02x faster                                                        |
| regex_compile  | 141 ms                                                                 | 139 ms: 1.01x faster                                                         |
| regex_effbot   | 3.67 ms                                                                | 3.71 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 237 us                                                                 | 221 us: 1.07x faster                                                         |
| tomli_loads          | 2.03 sec                                                               | 1.92 sec: 1.06x faster                                                       |
| unpickle             | 15.5 us                                                                | 15.0 us: 1.03x faster                                                        |
| xml_etree_process    | 60.1 ms                                                                | 59.2 ms: 1.02x faster                                                        |
| pickle_pure_python   | 308 us                                                                 | 304 us: 1.01x faster                                                         |
| xml_etree_iterparse  | 104 ms                                                                 | 103 ms: 1.01x faster                                                         |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                        |
| xml_etree_generate   | 87.3 ms                                                                | 86.7 ms: 1.01x faster                                                        |
| json_loads           | 27.3 us                                                                | 27.5 us: 1.01x slower                                                        |
| pickle               | 11.6 us                                                                | 11.9 us: 1.03x slower                                                        |
| unpickle_list        | 5.16 us                                                                | 5.42 us: 1.05x slower                                                        |
| pickle_list          | 5.11 us                                                                | 5.38 us: 1.05x slower                                                        |
| pickle_dict          | 34.0 us                                                                | 36.8 us: 1.08x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| python_startup_no_site | 7.57 ms                                                                | 7.63 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.1 ms: 1.07x faster                                                        |
| django_template | 36.4 ms                                                                | 35.6 ms: 1.02x faster                                                        |
| genshi_text     | 24.5 ms                                                                | 24.1 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody                    | 90.4 ms                                                                | 77.3 ms: 1.17x faster                                                        |
| spectral_norm            | 114 ms                                                                 | 97.7 ms: 1.16x faster                                                        |
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.29 ms: 1.16x faster                                                        |
| scimark_fft              | 344 ms                                                                 | 302 ms: 1.14x faster                                                         |
| fannkuch                 | 386 ms                                                                 | 349 ms: 1.11x faster                                                         |
| scimark_monte_carlo      | 70.0 ms                                                                | 63.3 ms: 1.11x faster                                                        |
| gc_traversal             | 4.01 ms                                                                | 3.70 ms: 1.08x faster                                                        |
| crypto_pyaes             | 73.3 ms                                                                | 68.3 ms: 1.07x faster                                                        |
| unpickle_pure_python     | 237 us                                                                 | 221 us: 1.07x faster                                                         |
| scimark_lu               | 132 ms                                                                 | 124 ms: 1.07x faster                                                         |
| float                    | 77.2 ms                                                                | 72.4 ms: 1.07x faster                                                        |
| mako                     | 10.8 ms                                                                | 10.1 ms: 1.07x faster                                                        |
| pprint_safe_repr         | 763 ms                                                                 | 718 ms: 1.06x faster                                                         |
| tomli_loads              | 2.03 sec                                                               | 1.92 sec: 1.06x faster                                                       |
| logging_silent           | 108 ns                                                                 | 102 ns: 1.06x faster                                                         |
| nqueens                  | 89.8 ms                                                                | 85.1 ms: 1.06x faster                                                        |
| regex_dna                | 230 ms                                                                 | 218 ms: 1.05x faster                                                         |
| typing_runtime_protocols | 117 us                                                                 | 111 us: 1.05x faster                                                         |
| go                       | 155 ms                                                                 | 147 ms: 1.05x faster                                                         |
| hexiom                   | 6.88 ms                                                                | 6.56 ms: 1.05x faster                                                        |
| richards                 | 43.7 ms                                                                | 42.0 ms: 1.04x faster                                                        |
| chaos                    | 63.4 ms                                                                | 60.8 ms: 1.04x faster                                                        |
| comprehensions           | 17.7 us                                                                | 17.1 us: 1.04x faster                                                        |
| chameleon                | 7.11 ms                                                                | 6.88 ms: 1.03x faster                                                        |
| pprint_pformat           | 1.55 sec                                                               | 1.50 sec: 1.03x faster                                                       |
| pyflate                  | 463 ms                                                                 | 450 ms: 1.03x faster                                                         |
| unpickle                 | 15.5 us                                                                | 15.0 us: 1.03x faster                                                        |
| pycparser                | 1.19 sec                                                               | 1.16 sec: 1.03x faster                                                       |
| richards_super           | 49.4 ms                                                                | 48.2 ms: 1.03x faster                                                        |
| telco                    | 8.73 ms                                                                | 8.53 ms: 1.02x faster                                                        |
| django_template          | 36.4 ms                                                                | 35.6 ms: 1.02x faster                                                        |
| deepcopy_reduce          | 3.22 us                                                                | 3.16 us: 1.02x faster                                                        |
| mdp                      | 2.68 sec                                                               | 2.63 sec: 1.02x faster                                                       |
| regex_v8                 | 25.2 ms                                                                | 24.7 ms: 1.02x faster                                                        |
| deepcopy_memo            | 39.2 us                                                                | 38.4 us: 1.02x faster                                                        |
| meteor_contest           | 111 ms                                                                 | 109 ms: 1.02x faster                                                         |
| scimark_sor              | 134 ms                                                                 | 132 ms: 1.02x faster                                                         |
| sympy_str                | 295 ms                                                                 | 290 ms: 1.02x faster                                                         |
| xml_etree_process        | 60.1 ms                                                                | 59.2 ms: 1.02x faster                                                        |
| sqlglot_parse            | 1.32 ms                                                                | 1.30 ms: 1.02x faster                                                        |
| genshi_text              | 24.5 ms                                                                | 24.1 ms: 1.01x faster                                                        |
| sqlglot_transpile        | 1.65 ms                                                                | 1.63 ms: 1.01x faster                                                        |
| pickle_pure_python       | 308 us                                                                 | 304 us: 1.01x faster                                                         |
| regex_compile            | 141 ms                                                                 | 139 ms: 1.01x faster                                                         |
| sympy_integrate          | 22.0 ms                                                                | 21.8 ms: 1.01x faster                                                        |
| sympy_sum                | 168 ms                                                                 | 166 ms: 1.01x faster                                                         |
| html5lib                 | 68.8 ms                                                                | 68.0 ms: 1.01x faster                                                        |
| xml_etree_iterparse      | 104 ms                                                                 | 103 ms: 1.01x faster                                                         |
| json                     | 5.10 ms                                                                | 5.05 ms: 1.01x faster                                                        |
| generators               | 30.3 ms                                                                | 30.0 ms: 1.01x faster                                                        |
| deepcopy                 | 361 us                                                                 | 358 us: 1.01x faster                                                         |
| json_dumps               | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                        |
| asyncio_tcp              | 509 ms                                                                 | 504 ms: 1.01x faster                                                         |
| sqlglot_optimize         | 57.2 ms                                                                | 56.7 ms: 1.01x faster                                                        |
| create_gc_cycles         | 1.77 ms                                                                | 1.75 ms: 1.01x faster                                                        |
| 2to3                     | 277 ms                                                                 | 275 ms: 1.01x faster                                                         |
| xml_etree_generate       | 87.3 ms                                                                | 86.7 ms: 1.01x faster                                                        |
| docutils                 | 2.91 sec                                                               | 2.89 sec: 1.00x faster                                                       |
| sqlglot_normalize        | 113 ms                                                                 | 112 ms: 1.00x faster                                                         |
| pidigits                 | 189 ms                                                                 | 189 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                       |
| bench_thread_pool        | 859 us                                                                 | 862 us: 1.00x slower                                                         |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| json_loads               | 27.3 us                                                                | 27.5 us: 1.01x slower                                                        |
| regex_effbot             | 3.67 ms                                                                | 3.71 ms: 1.01x slower                                                        |
| python_startup_no_site   | 7.57 ms                                                                | 7.63 ms: 1.01x slower                                                        |
| raytrace                 | 273 ms                                                                 | 276 ms: 1.01x slower                                                         |
| pathlib                  | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                        |
| async_generators         | 462 ms                                                                 | 470 ms: 1.02x slower                                                         |
| pickle                   | 11.6 us                                                                | 11.9 us: 1.03x slower                                                        |
| unpickle_list            | 5.16 us                                                                | 5.42 us: 1.05x slower                                                        |
| pickle_list              | 5.11 us                                                                | 5.38 us: 1.05x slower                                                        |
| pickle_dict              | 34.0 us                                                                | 36.8 us: 1.08x slower                                                        |
| Geometric mean           | (ref)                                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (28): deltablue, async_tree_none, async_tree_io_tg, pylint, xml_etree_parse, dask, async_tree_none_tg, mypy2, aiohttp, sqlite_synth, async_tree_cpu_io_mixed_tg, sympy_expand, coroutines, dulwich_log, thrift, async_tree_cpu_io_mixed, async_tree_memoization, asyncio_websockets, gunicorn, async_tree_memoization_tg, genshi_xml, bench_mp_pool, tornado_http, logging_format, async_tree_io, coverage, logging_simple, djangocms

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache_3
- machine: linux-x86_64
- commit hash: a9d8d6e
- commit date: 2024-04-23
- overall geometric mean: 1.02x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 275 ms: 1.01x faster                                                         |
| chameleon      | 7.11 ms                                                                | 6.97 ms: 1.02x faster                                                        |
| html5lib       | 68.8 ms                                                                | 67.9 ms: 1.01x faster                                                        |
| tornado_http   | 95.9 ms                                                                | 96.6 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|--------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg | 341 ms                                                                 | 335 ms: 1.02x faster                                                         |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 76.0 ms: 1.19x faster                                                        |
| float          | 77.2 ms                                                                | 73.1 ms: 1.06x faster                                                        |
| pidigits       | 189 ms                                                                 | 189 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 230 ms                                                                 | 221 ms: 1.04x faster                                                         |
| regex_v8       | 25.2 ms                                                                | 24.5 ms: 1.03x faster                                                        |
| regex_effbot   | 3.67 ms                                                                | 3.76 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.03 sec                                                               | 1.90 sec: 1.07x faster                                                       |
| unpickle_pure_python | 237 us                                                                 | 224 us: 1.06x faster                                                         |
| xml_etree_parse      | 152 ms                                                                 | 149 ms: 1.02x faster                                                         |
| xml_etree_iterparse  | 104 ms                                                                 | 103 ms: 1.01x faster                                                         |
| pickle_pure_python   | 308 us                                                                 | 306 us: 1.01x faster                                                         |
| xml_etree_generate   | 87.3 ms                                                                | 87.1 ms: 1.00x faster                                                        |
| pickle_list          | 5.11 us                                                                | 5.18 us: 1.02x slower                                                        |
| json_loads           | 27.3 us                                                                | 27.7 us: 1.02x slower                                                        |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                        |
| pickle               | 11.6 us                                                                | 11.8 us: 1.02x slower                                                        |
| pickle_dict          | 34.0 us                                                                | 34.8 us: 1.02x slower                                                        |
| unpickle_list        | 5.16 us                                                                | 5.31 us: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (2): unpickle, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| python_startup_no_site | 7.57 ms                                                                | 7.65 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.0 ms: 1.08x faster                                                        |
| django_template | 36.4 ms                                                                | 35.9 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody                    | 90.4 ms                                                                | 76.0 ms: 1.19x faster                                                        |
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.22 ms: 1.18x faster                                                        |
| spectral_norm            | 114 ms                                                                 | 99.2 ms: 1.14x faster                                                        |
| scimark_fft              | 344 ms                                                                 | 302 ms: 1.14x faster                                                         |
| scimark_monte_carlo      | 70.0 ms                                                                | 62.6 ms: 1.12x faster                                                        |
| fannkuch                 | 386 ms                                                                 | 349 ms: 1.11x faster                                                         |
| crypto_pyaes             | 73.3 ms                                                                | 67.9 ms: 1.08x faster                                                        |
| mako                     | 10.8 ms                                                                | 10.0 ms: 1.08x faster                                                        |
| scimark_lu               | 132 ms                                                                 | 123 ms: 1.07x faster                                                         |
| tomli_loads              | 2.03 sec                                                               | 1.90 sec: 1.07x faster                                                       |
| logging_silent           | 108 ns                                                                 | 101 ns: 1.06x faster                                                         |
| unpickle_pure_python     | 237 us                                                                 | 224 us: 1.06x faster                                                         |
| float                    | 77.2 ms                                                                | 73.1 ms: 1.06x faster                                                        |
| scimark_sor              | 134 ms                                                                 | 128 ms: 1.05x faster                                                         |
| chaos                    | 63.4 ms                                                                | 60.6 ms: 1.05x faster                                                        |
| regex_dna                | 230 ms                                                                 | 221 ms: 1.04x faster                                                         |
| hexiom                   | 6.88 ms                                                                | 6.61 ms: 1.04x faster                                                        |
| go                       | 155 ms                                                                 | 149 ms: 1.04x faster                                                         |
| pprint_pformat           | 1.55 sec                                                               | 1.49 sec: 1.04x faster                                                       |
| pyflate                  | 463 ms                                                                 | 447 ms: 1.04x faster                                                         |
| pprint_safe_repr         | 763 ms                                                                 | 738 ms: 1.03x faster                                                         |
| nqueens                  | 89.8 ms                                                                | 87.1 ms: 1.03x faster                                                        |
| regex_v8                 | 25.2 ms                                                                | 24.5 ms: 1.03x faster                                                        |
| telco                    | 8.73 ms                                                                | 8.53 ms: 1.02x faster                                                        |
| pycparser                | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                       |
| chameleon                | 7.11 ms                                                                | 6.97 ms: 1.02x faster                                                        |
| async_tree_none_tg       | 341 ms                                                                 | 335 ms: 1.02x faster                                                         |
| generators               | 30.3 ms                                                                | 29.7 ms: 1.02x faster                                                        |
| typing_runtime_protocols | 117 us                                                                 | 115 us: 1.02x faster                                                         |
| comprehensions           | 17.7 us                                                                | 17.4 us: 1.02x faster                                                        |
| xml_etree_parse          | 152 ms                                                                 | 149 ms: 1.02x faster                                                         |
| django_template          | 36.4 ms                                                                | 35.9 ms: 1.01x faster                                                        |
| html5lib                 | 68.8 ms                                                                | 67.9 ms: 1.01x faster                                                        |
| richards                 | 43.7 ms                                                                | 43.2 ms: 1.01x faster                                                        |
| mdp                      | 2.68 sec                                                               | 2.65 sec: 1.01x faster                                                       |
| meteor_contest           | 111 ms                                                                 | 110 ms: 1.01x faster                                                         |
| xml_etree_iterparse      | 104 ms                                                                 | 103 ms: 1.01x faster                                                         |
| sqlite_synth             | 2.86 us                                                                | 2.84 us: 1.01x faster                                                        |
| 2to3                     | 277 ms                                                                 | 275 ms: 1.01x faster                                                         |
| pickle_pure_python       | 308 us                                                                 | 306 us: 1.01x faster                                                         |
| sqlglot_transpile        | 1.65 ms                                                                | 1.64 ms: 1.01x faster                                                        |
| xml_etree_generate       | 87.3 ms                                                                | 87.1 ms: 1.00x faster                                                        |
| pidigits                 | 189 ms                                                                 | 189 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                       |
| tornado_http             | 95.9 ms                                                                | 96.6 ms: 1.01x slower                                                        |
| deepcopy_memo            | 39.2 us                                                                | 39.5 us: 1.01x slower                                                        |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                        |
| python_startup_no_site   | 7.57 ms                                                                | 7.65 ms: 1.01x slower                                                        |
| pathlib                  | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                        |
| gc_traversal             | 4.01 ms                                                                | 4.06 ms: 1.01x slower                                                        |
| dulwich_log              | 69.3 ms                                                                | 70.1 ms: 1.01x slower                                                        |
| asyncio_tcp              | 509 ms                                                                 | 516 ms: 1.01x slower                                                         |
| raytrace                 | 273 ms                                                                 | 277 ms: 1.01x slower                                                         |
| async_generators         | 462 ms                                                                 | 468 ms: 1.01x slower                                                         |
| sqlglot_normalize        | 113 ms                                                                 | 114 ms: 1.01x slower                                                         |
| bench_thread_pool        | 859 us                                                                 | 872 us: 1.01x slower                                                         |
| thrift                   | 823 us                                                                 | 836 us: 1.01x slower                                                         |
| pickle_list              | 5.11 us                                                                | 5.18 us: 1.02x slower                                                        |
| logging_format           | 6.47 us                                                                | 6.57 us: 1.02x slower                                                        |
| json_loads               | 27.3 us                                                                | 27.7 us: 1.02x slower                                                        |
| coverage                 | 96.7 ms                                                                | 98.4 ms: 1.02x slower                                                        |
| json_dumps               | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                        |
| json                     | 5.10 ms                                                                | 5.20 ms: 1.02x slower                                                        |
| pickle                   | 11.6 us                                                                | 11.8 us: 1.02x slower                                                        |
| logging_simple           | 5.81 us                                                                | 5.93 us: 1.02x slower                                                        |
| pickle_dict              | 34.0 us                                                                | 34.8 us: 1.02x slower                                                        |
| regex_effbot             | 3.67 ms                                                                | 3.76 ms: 1.02x slower                                                        |
| unpickle_list            | 5.16 us                                                                | 5.31 us: 1.03x slower                                                        |
| Geometric mean           | (ref)                                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (33): async_tree_none, async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed_tg, unpickle, async_tree_cpu_io_mixed, async_tree_memoization_tg, dask, asyncio_websockets, sympy_sum, xml_etree_process, pylint, sympy_str, deltablue, sqlglot_parse, docutils, deepcopy, create_gc_cycles, sqlglot_optimize, regex_compile, coroutines, richards_super, genshi_xml, sympy_integrate, sympy_expand, bench_mp_pool, mypy2, deepcopy_reduce, gunicorn, genshi_text, aiohttp, djangocms, async_tree_memoization

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x
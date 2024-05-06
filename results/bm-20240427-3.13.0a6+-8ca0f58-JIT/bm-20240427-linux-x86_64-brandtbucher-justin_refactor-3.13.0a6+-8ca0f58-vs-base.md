# Results vs. base

- fork: brandtbucher
- ref: justin_refactor
- machine: linux-x86_64
- commit hash: 8ca0f58
- commit date: 2024-04-27
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 276 ms: 1.00x faster                                                    |
| chameleon      | 7.11 ms                                                                | 7.02 ms: 1.01x faster                                                   |
| html5lib       | 68.8 ms                                                                | 67.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|--------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg | 341 ms                                                                 | 335 ms: 1.02x faster                                                    |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 89.9 ms: 1.01x faster                                                   |
| pidigits       | 189 ms                                                                 | 189 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 230 ms                                                                 | 227 ms: 1.02x faster                                                    |
| regex_compile  | 141 ms                                                                 | 140 ms: 1.01x faster                                                    |
| regex_effbot   | 3.67 ms                                                                | 3.70 ms: 1.01x slower                                                   |
| regex_v8       | 25.2 ms                                                                | 26.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 308 us                                                                 | 301 us: 1.02x faster                                                    |
| unpickle_pure_python | 237 us                                                                 | 233 us: 1.02x faster                                                    |
| pickle               | 11.6 us                                                                | 11.5 us: 1.01x faster                                                   |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| xml_etree_process    | 60.1 ms                                                                | 59.6 ms: 1.01x faster                                                   |
| pickle_list          | 5.11 us                                                                | 5.08 us: 1.01x faster                                                   |
| xml_etree_generate   | 87.3 ms                                                                | 87.0 ms: 1.00x faster                                                   |
| xml_etree_iterparse  | 104 ms                                                                 | 104 ms: 1.01x slower                                                    |
| unpickle_list        | 5.16 us                                                                | 5.20 us: 1.01x slower                                                   |
| json_loads           | 27.3 us                                                                | 28.0 us: 1.03x slower                                                   |
| pickle_dict          | 34.0 us                                                                | 35.1 us: 1.03x slower                                                   |
| unpickle             | 15.5 us                                                                | 16.3 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 36.4 ms                                                                | 35.7 ms: 1.02x faster                                                   |
| genshi_xml      | 53.7 ms                                                                | 53.3 ms: 1.01x faster                                                   |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| logging_silent           | 108 ns                                                                 | 98.0 ns: 1.10x faster                                                   |
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.69 ms: 1.06x faster                                                   |
| scimark_sor              | 134 ms                                                                 | 130 ms: 1.03x faster                                                    |
| deepcopy_memo            | 39.2 us                                                                | 37.9 us: 1.03x faster                                                   |
| pprint_safe_repr         | 763 ms                                                                 | 740 ms: 1.03x faster                                                    |
| typing_runtime_protocols | 117 us                                                                 | 113 us: 1.03x faster                                                    |
| deltablue                | 3.73 ms                                                                | 3.62 ms: 1.03x faster                                                   |
| deepcopy                 | 361 us                                                                 | 353 us: 1.02x faster                                                    |
| pickle_pure_python       | 308 us                                                                 | 301 us: 1.02x faster                                                    |
| scimark_fft              | 344 ms                                                                 | 336 ms: 1.02x faster                                                    |
| telco                    | 8.73 ms                                                                | 8.56 ms: 1.02x faster                                                   |
| html5lib                 | 68.8 ms                                                                | 67.5 ms: 1.02x faster                                                   |
| django_template          | 36.4 ms                                                                | 35.7 ms: 1.02x faster                                                   |
| async_tree_none_tg       | 341 ms                                                                 | 335 ms: 1.02x faster                                                    |
| unpickle_pure_python     | 237 us                                                                 | 233 us: 1.02x faster                                                    |
| regex_dna                | 230 ms                                                                 | 227 ms: 1.02x faster                                                    |
| go                       | 155 ms                                                                 | 153 ms: 1.01x faster                                                    |
| deepcopy_reduce          | 3.22 us                                                                | 3.17 us: 1.01x faster                                                   |
| generators               | 30.3 ms                                                                | 29.8 ms: 1.01x faster                                                   |
| sympy_sum                | 168 ms                                                                 | 165 ms: 1.01x faster                                                    |
| richards                 | 43.7 ms                                                                | 43.1 ms: 1.01x faster                                                   |
| nqueens                  | 89.8 ms                                                                | 88.6 ms: 1.01x faster                                                   |
| dask                     | 378 ms                                                                 | 373 ms: 1.01x faster                                                    |
| sympy_str                | 295 ms                                                                 | 291 ms: 1.01x faster                                                    |
| chameleon                | 7.11 ms                                                                | 7.02 ms: 1.01x faster                                                   |
| scimark_monte_carlo      | 70.0 ms                                                                | 69.1 ms: 1.01x faster                                                   |
| scimark_lu               | 132 ms                                                                 | 130 ms: 1.01x faster                                                    |
| sympy_integrate          | 22.0 ms                                                                | 21.8 ms: 1.01x faster                                                   |
| sqlglot_normalize        | 113 ms                                                                 | 111 ms: 1.01x faster                                                    |
| sqlglot_transpile        | 1.65 ms                                                                | 1.63 ms: 1.01x faster                                                   |
| sympy_expand             | 494 ms                                                                 | 489 ms: 1.01x faster                                                    |
| spectral_norm            | 114 ms                                                                 | 112 ms: 1.01x faster                                                    |
| pyflate                  | 463 ms                                                                 | 459 ms: 1.01x faster                                                    |
| pickle                   | 11.6 us                                                                | 11.5 us: 1.01x faster                                                   |
| sqlglot_optimize         | 57.2 ms                                                                | 56.7 ms: 1.01x faster                                                   |
| json_dumps               | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| bench_thread_pool        | 859 us                                                                 | 852 us: 1.01x faster                                                    |
| richards_super           | 49.4 ms                                                                | 49.0 ms: 1.01x faster                                                   |
| thrift                   | 823 us                                                                 | 817 us: 1.01x faster                                                    |
| xml_etree_process        | 60.1 ms                                                                | 59.6 ms: 1.01x faster                                                   |
| genshi_xml               | 53.7 ms                                                                | 53.3 ms: 1.01x faster                                                   |
| nbody                    | 90.4 ms                                                                | 89.9 ms: 1.01x faster                                                   |
| regex_compile            | 141 ms                                                                 | 140 ms: 1.01x faster                                                    |
| sqlglot_parse            | 1.32 ms                                                                | 1.32 ms: 1.01x faster                                                   |
| pickle_list              | 5.11 us                                                                | 5.08 us: 1.01x faster                                                   |
| 2to3                     | 277 ms                                                                 | 276 ms: 1.00x faster                                                    |
| xml_etree_generate       | 87.3 ms                                                                | 87.0 ms: 1.00x faster                                                   |
| create_gc_cycles         | 1.77 ms                                                                | 1.76 ms: 1.00x faster                                                   |
| pidigits                 | 189 ms                                                                 | 189 ms: 1.00x faster                                                    |
| crypto_pyaes             | 73.3 ms                                                                | 73.7 ms: 1.01x slower                                                   |
| xml_etree_iterparse      | 104 ms                                                                 | 104 ms: 1.01x slower                                                    |
| unpickle_list            | 5.16 us                                                                | 5.20 us: 1.01x slower                                                   |
| regex_effbot             | 3.67 ms                                                                | 3.70 ms: 1.01x slower                                                   |
| sqlite_synth             | 2.86 us                                                                | 2.89 us: 1.01x slower                                                   |
| comprehensions           | 17.7 us                                                                | 17.9 us: 1.01x slower                                                   |
| pycparser                | 1.19 sec                                                               | 1.21 sec: 1.02x slower                                                  |
| coverage                 | 96.7 ms                                                                | 98.7 ms: 1.02x slower                                                   |
| json_loads               | 27.3 us                                                                | 28.0 us: 1.03x slower                                                   |
| pickle_dict              | 34.0 us                                                                | 35.1 us: 1.03x slower                                                   |
| mdp                      | 2.68 sec                                                               | 2.78 sec: 1.04x slower                                                  |
| regex_v8                 | 25.2 ms                                                                | 26.2 ms: 1.04x slower                                                   |
| unpickle                 | 15.5 us                                                                | 16.3 us: 1.05x slower                                                   |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (39): async_tree_cpu_io_mixed, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization_tg, async_tree_io_tg, logging_simple, logging_format, genshi_text, meteor_contest, mypy2, pylint, aiohttp, chaos, raytrace, hexiom, tornado_http, dulwich_log, docutils, pprint_pformat, gunicorn, async_generators, gc_traversal, python_startup, asyncio_websockets, python_startup_no_site, asyncio_tcp, float, mako, asyncio_tcp_ssl, fannkuch, coroutines, pathlib, tomli_loads, json, async_tree_memoization, bench_mp_pool, xml_etree_parse, djangocms

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 7a3c89e
- commit date: 2024-04-04
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                       | 300 ms: 1.00x slower                                                      |
| chameleon      | 7.43 ms                                                                      | 7.26 ms: 1.02x faster                                                     |
| tornado_http   | 124 ms                                                                       | 122 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 377 ms                                                                       | 358 ms: 1.05x faster                                                      |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 576 ms: 1.04x faster                                                      |
| async_tree_io              | 907 ms                                                                       | 886 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed    | 600 ms                                                                       | 595 ms: 1.01x faster                                                      |
| async_tree_io_tg           | 880 ms                                                                       | 910 ms: 1.03x slower                                                      |
| Geometric mean             | (ref)                                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 79.5 ms                                                                      | 76.4 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                      | 25.5 ms: 1.02x faster                                                     |
| regex_dna      | 244 ms                                                                       | 242 ms: 1.01x faster                                                      |
| regex_effbot   | 3.42 ms                                                                      | 3.72 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_pure_python   | 316 us                                                                       | 305 us: 1.03x faster                                                      |
| unpickle             | 15.5 us                                                                      | 15.1 us: 1.03x faster                                                     |
| json_loads           | 25.8 us                                                                      | 25.3 us: 1.02x faster                                                     |
| unpickle_pure_python | 235 us                                                                       | 233 us: 1.01x faster                                                      |
| xml_etree_parse      | 144 ms                                                                       | 143 ms: 1.01x faster                                                      |
| pickle_dict          | 33.0 us                                                                      | 32.9 us: 1.01x faster                                                     |
| xml_etree_iterparse  | 104 ms                                                                       | 103 ms: 1.00x faster                                                      |
| pickle               | 10.9 us                                                                      | 10.9 us: 1.01x slower                                                     |
| xml_etree_process    | 58.5 ms                                                                      | 59.0 ms: 1.01x slower                                                     |
| xml_etree_generate   | 83.9 ms                                                                      | 84.9 ms: 1.01x slower                                                     |
| json_dumps           | 10.5 ms                                                                      | 10.8 ms: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                                        | 1.00x faster                                                              |

Benchmark hidden because not significant (3): tomli_loads, unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|-----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 41.2 ms                                                                      | 39.9 ms: 1.03x faster                                                     |
| genshi_xml      | 59.1 ms                                                                      | 57.5 ms: 1.03x faster                                                     |
| genshi_text     | 26.8 ms                                                                      | 26.4 ms: 1.01x faster                                                     |
| mako            | 10.0 ms                                                                      | 9.96 ms: 1.00x faster                                                     |
| Geometric mean  | (ref)                                                                        | 1.02x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 377 ms                                                                       | 358 ms: 1.05x faster                                                      |
| pyflate                    | 519 ms                                                                       | 496 ms: 1.05x faster                                                      |
| go                         | 180 ms                                                                       | 173 ms: 1.04x faster                                                      |
| float                      | 79.5 ms                                                                      | 76.4 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 576 ms: 1.04x faster                                                      |
| django_template            | 41.2 ms                                                                      | 39.9 ms: 1.03x faster                                                     |
| richards                   | 51.9 ms                                                                      | 50.2 ms: 1.03x faster                                                     |
| pickle_pure_python         | 316 us                                                                       | 305 us: 1.03x faster                                                      |
| sqlglot_parse              | 1.45 ms                                                                      | 1.40 ms: 1.03x faster                                                     |
| generators                 | 34.6 ms                                                                      | 33.5 ms: 1.03x faster                                                     |
| pycparser                  | 1.29 sec                                                                     | 1.25 sec: 1.03x faster                                                    |
| deltablue                  | 3.85 ms                                                                      | 3.72 ms: 1.03x faster                                                     |
| coverage                   | 83.0 ms                                                                      | 80.6 ms: 1.03x faster                                                     |
| sqlglot_transpile          | 1.84 ms                                                                      | 1.79 ms: 1.03x faster                                                     |
| unpickle                   | 15.5 us                                                                      | 15.1 us: 1.03x faster                                                     |
| genshi_xml                 | 59.1 ms                                                                      | 57.5 ms: 1.03x faster                                                     |
| regex_v8                   | 26.1 ms                                                                      | 25.5 ms: 1.02x faster                                                     |
| logging_simple             | 6.80 us                                                                      | 6.64 us: 1.02x faster                                                     |
| async_tree_io              | 907 ms                                                                       | 886 ms: 1.02x faster                                                      |
| chameleon                  | 7.43 ms                                                                      | 7.26 ms: 1.02x faster                                                     |
| sqlglot_normalize          | 125 ms                                                                       | 122 ms: 1.02x faster                                                      |
| tornado_http               | 124 ms                                                                       | 122 ms: 1.02x faster                                                      |
| typing_runtime_protocols   | 122 us                                                                       | 120 us: 1.02x faster                                                      |
| json_loads                 | 25.8 us                                                                      | 25.3 us: 1.02x faster                                                     |
| richards_super             | 58.0 ms                                                                      | 57.1 ms: 1.02x faster                                                     |
| genshi_text                | 26.8 ms                                                                      | 26.4 ms: 1.01x faster                                                     |
| sympy_integrate            | 25.3 ms                                                                      | 25.0 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 4.15 ms                                                                      | 4.09 ms: 1.01x faster                                                     |
| chaos                      | 67.5 ms                                                                      | 66.6 ms: 1.01x faster                                                     |
| sqlglot_optimize           | 63.6 ms                                                                      | 62.8 ms: 1.01x faster                                                     |
| async_generators           | 390 ms                                                                       | 385 ms: 1.01x faster                                                      |
| deepcopy                   | 388 us                                                                       | 384 us: 1.01x faster                                                      |
| sympy_expand               | 512 ms                                                                       | 507 ms: 1.01x faster                                                      |
| raytrace                   | 308 ms                                                                       | 305 ms: 1.01x faster                                                      |
| scimark_sor                | 154 ms                                                                       | 153 ms: 1.01x faster                                                      |
| async_tree_cpu_io_mixed    | 600 ms                                                                       | 595 ms: 1.01x faster                                                      |
| unpickle_pure_python       | 235 us                                                                       | 233 us: 1.01x faster                                                      |
| pprint_safe_repr           | 841 ms                                                                       | 834 ms: 1.01x faster                                                      |
| sympy_sum                  | 163 ms                                                                       | 161 ms: 1.01x faster                                                      |
| xml_etree_parse            | 144 ms                                                                       | 143 ms: 1.01x faster                                                      |
| gc_traversal               | 4.38 ms                                                                      | 4.35 ms: 1.01x faster                                                     |
| sympy_str                  | 304 ms                                                                       | 301 ms: 1.01x faster                                                      |
| json                       | 5.41 ms                                                                      | 5.37 ms: 1.01x faster                                                     |
| regex_dna                  | 244 ms                                                                       | 242 ms: 1.01x faster                                                      |
| hexiom                     | 7.57 ms                                                                      | 7.52 ms: 1.01x faster                                                     |
| pickle_dict                | 33.0 us                                                                      | 32.9 us: 1.01x faster                                                     |
| mako                       | 10.0 ms                                                                      | 9.96 ms: 1.00x faster                                                     |
| xml_etree_iterparse        | 104 ms                                                                       | 103 ms: 1.00x faster                                                      |
| deepcopy_memo              | 38.3 us                                                                      | 38.2 us: 1.00x faster                                                     |
| nqueens                    | 103 ms                                                                       | 103 ms: 1.00x faster                                                      |
| asyncio_tcp_ssl            | 1.58 sec                                                                     | 1.58 sec: 1.00x slower                                                    |
| 2to3                       | 300 ms                                                                       | 300 ms: 1.00x slower                                                      |
| create_gc_cycles           | 1.79 ms                                                                      | 1.79 ms: 1.00x slower                                                     |
| pickle                     | 10.9 us                                                                      | 10.9 us: 1.01x slower                                                     |
| xml_etree_process          | 58.5 ms                                                                      | 59.0 ms: 1.01x slower                                                     |
| xml_etree_generate         | 83.9 ms                                                                      | 84.9 ms: 1.01x slower                                                     |
| scimark_monte_carlo        | 72.9 ms                                                                      | 73.7 ms: 1.01x slower                                                     |
| mdp                        | 2.62 sec                                                                     | 2.65 sec: 1.01x slower                                                    |
| spectral_norm              | 93.2 ms                                                                      | 94.3 ms: 1.01x slower                                                     |
| fannkuch                   | 379 ms                                                                       | 384 ms: 1.01x slower                                                      |
| thrift                     | 882 us                                                                       | 893 us: 1.01x slower                                                      |
| meteor_contest             | 131 ms                                                                       | 132 ms: 1.01x slower                                                      |
| deepcopy_reduce            | 3.40 us                                                                      | 3.45 us: 1.01x slower                                                     |
| telco                      | 7.97 ms                                                                      | 8.22 ms: 1.03x slower                                                     |
| json_dumps                 | 10.5 ms                                                                      | 10.8 ms: 1.03x slower                                                     |
| async_tree_io_tg           | 880 ms                                                                       | 910 ms: 1.03x slower                                                      |
| regex_effbot               | 3.42 ms                                                                      | 3.72 ms: 1.09x slower                                                     |
| Geometric mean             | (ref)                                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (33): async_tree_memoization, mypy2, async_tree_none_tg, pprint_pformat, scimark_lu, dask, logging_format, gunicorn, coroutines, nbody, bench_mp_pool, sqlite_synth, tomli_loads, docutils, pylint, dulwich_log, logging_silent, pathlib, bench_thread_pool, crypto_pyaes, asyncio_tcp, comprehensions, aiohttp, pidigits, python_startup, asyncio_websockets, python_startup_no_site, regex_compile, html5lib, unpickle_list, scimark_fft, pickle_list, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
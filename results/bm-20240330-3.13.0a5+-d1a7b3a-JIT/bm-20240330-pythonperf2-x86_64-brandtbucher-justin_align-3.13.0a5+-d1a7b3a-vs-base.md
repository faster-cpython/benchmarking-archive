# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.00x slower
- HPT reliability: 58.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                       | 299 ms: 1.00x slower                                                       |
| chameleon      | 7.35 ms                                                                      | 7.12 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                               |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 261 ms                                                                       | 261 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                               |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.48 ms                                                                      | 3.46 ms: 1.01x faster                                                      |
| regex_dna      | 238 ms                                                                       | 238 ms: 1.00x slower                                                       |
| regex_compile  | 146 ms                                                                       | 147 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                               |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle             | 15.2 us                                                                      | 14.8 us: 1.03x faster                                                      |
| unpickle_list        | 4.74 us                                                                      | 4.60 us: 1.03x faster                                                      |
| xml_etree_generate   | 84.6 ms                                                                      | 83.4 ms: 1.02x faster                                                      |
| tomli_loads          | 2.16 sec                                                                     | 2.14 sec: 1.01x faster                                                     |
| json_loads           | 25.4 us                                                                      | 25.3 us: 1.01x faster                                                      |
| xml_etree_iterparse  | 103 ms                                                                       | 103 ms: 1.00x faster                                                       |
| unpickle_pure_python | 232 us                                                                       | 235 us: 1.02x slower                                                       |
| pickle_pure_python   | 307 us                                                                       | 315 us: 1.03x slower                                                       |
| pickle_list          | 4.31 us                                                                      | 4.50 us: 1.04x slower                                                      |
| pickle_dict          | 30.8 us                                                                      | 33.6 us: 1.09x slower                                                      |
| Geometric mean       | (ref)                                                                        | 1.01x slower                                                               |

Benchmark hidden because not significant (4): pickle, xml_etree_process, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.7 ms: 1.00x faster                                                      |
| python_startup         | 13.5 ms                                                                      | 13.5 ms: 1.00x faster                                                      |
| Geometric mean         | (ref)                                                                        | 1.00x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 9.97 ms                                                                      | 9.91 ms: 1.01x faster                                                      |
| genshi_xml     | 57.0 ms                                                                      | 57.9 ms: 1.02x slower                                                      |
| genshi_text    | 26.0 ms                                                                      | 26.6 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pyflate                 | 515 ms                                                                       | 496 ms: 1.04x faster                                                       |
| scimark_sparse_mat_mult | 4.30 ms                                                                      | 4.14 ms: 1.04x faster                                                      |
| chameleon               | 7.35 ms                                                                      | 7.12 ms: 1.03x faster                                                      |
| unpickle                | 15.2 us                                                                      | 14.8 us: 1.03x faster                                                      |
| unpickle_list           | 4.74 us                                                                      | 4.60 us: 1.03x faster                                                      |
| pathlib                 | 19.6 ms                                                                      | 19.1 ms: 1.02x faster                                                      |
| unpack_sequence         | 60.3 ns                                                                      | 59.2 ns: 1.02x faster                                                      |
| deepcopy                | 385 us                                                                       | 379 us: 1.02x faster                                                       |
| richards                | 51.7 ms                                                                      | 50.9 ms: 1.02x faster                                                      |
| xml_etree_generate      | 84.6 ms                                                                      | 83.4 ms: 1.02x faster                                                      |
| dulwich_log             | 69.9 ms                                                                      | 68.9 ms: 1.01x faster                                                      |
| deepcopy_memo           | 37.9 us                                                                      | 37.4 us: 1.01x faster                                                      |
| pprint_safe_repr        | 841 ms                                                                       | 831 ms: 1.01x faster                                                       |
| gc_traversal            | 4.60 ms                                                                      | 4.55 ms: 1.01x faster                                                      |
| sqlite_synth            | 2.70 us                                                                      | 2.67 us: 1.01x faster                                                      |
| scimark_sor             | 154 ms                                                                       | 153 ms: 1.01x faster                                                       |
| asyncio_tcp             | 371 ms                                                                       | 368 ms: 1.01x faster                                                       |
| tomli_loads             | 2.16 sec                                                                     | 2.14 sec: 1.01x faster                                                     |
| mako                    | 9.97 ms                                                                      | 9.91 ms: 1.01x faster                                                      |
| sympy_str               | 303 ms                                                                       | 301 ms: 1.01x faster                                                       |
| regex_effbot            | 3.48 ms                                                                      | 3.46 ms: 1.01x faster                                                      |
| nqueens                 | 106 ms                                                                       | 105 ms: 1.01x faster                                                       |
| fannkuch                | 380 ms                                                                       | 378 ms: 1.01x faster                                                       |
| json_loads              | 25.4 us                                                                      | 25.3 us: 1.01x faster                                                      |
| xml_etree_iterparse     | 103 ms                                                                       | 103 ms: 1.00x faster                                                       |
| sympy_integrate         | 25.2 ms                                                                      | 25.1 ms: 1.00x faster                                                      |
| python_startup_no_site  | 11.8 ms                                                                      | 11.7 ms: 1.00x faster                                                      |
| python_startup          | 13.5 ms                                                                      | 13.5 ms: 1.00x faster                                                      |
| pidigits                | 261 ms                                                                       | 261 ms: 1.00x slower                                                       |
| regex_dna               | 238 ms                                                                       | 238 ms: 1.00x slower                                                       |
| asyncio_tcp_ssl         | 1.57 sec                                                                     | 1.58 sec: 1.00x slower                                                     |
| regex_compile           | 146 ms                                                                       | 147 ms: 1.00x slower                                                       |
| 2to3                    | 298 ms                                                                       | 299 ms: 1.00x slower                                                       |
| sympy_expand            | 509 ms                                                                       | 512 ms: 1.00x slower                                                       |
| spectral_norm           | 92.9 ms                                                                      | 93.5 ms: 1.01x slower                                                      |
| deepcopy_reduce         | 3.35 us                                                                      | 3.38 us: 1.01x slower                                                      |
| pylint                  | 335 ms                                                                       | 337 ms: 1.01x slower                                                       |
| sympy_sum               | 161 ms                                                                       | 162 ms: 1.01x slower                                                       |
| create_gc_cycles        | 1.78 ms                                                                      | 1.79 ms: 1.01x slower                                                      |
| pycparser               | 1.25 sec                                                                     | 1.26 sec: 1.01x slower                                                     |
| asyncio_websockets      | 387 ms                                                                       | 391 ms: 1.01x slower                                                       |
| thrift                  | 864 us                                                                       | 873 us: 1.01x slower                                                       |
| comprehensions          | 19.7 us                                                                      | 19.9 us: 1.01x slower                                                      |
| sqlglot_transpile       | 1.81 ms                                                                      | 1.83 ms: 1.01x slower                                                      |
| logging_silent          | 97.6 ns                                                                      | 98.8 ns: 1.01x slower                                                      |
| scimark_monte_carlo     | 73.7 ms                                                                      | 74.6 ms: 1.01x slower                                                      |
| aiohttp                 | 1.12 ms                                                                      | 1.13 ms: 1.01x slower                                                      |
| sqlglot_parse           | 1.42 ms                                                                      | 1.44 ms: 1.01x slower                                                      |
| genshi_xml              | 57.0 ms                                                                      | 57.9 ms: 1.02x slower                                                      |
| unpickle_pure_python    | 232 us                                                                       | 235 us: 1.02x slower                                                       |
| bench_thread_pool       | 1.10 ms                                                                      | 1.12 ms: 1.02x slower                                                      |
| generators              | 33.7 ms                                                                      | 34.3 ms: 1.02x slower                                                      |
| scimark_lu              | 119 ms                                                                       | 122 ms: 1.02x slower                                                       |
| pickle_pure_python      | 307 us                                                                       | 315 us: 1.03x slower                                                       |
| genshi_text             | 26.0 ms                                                                      | 26.6 ms: 1.03x slower                                                      |
| raytrace                | 302 ms                                                                       | 310 ms: 1.03x slower                                                       |
| pickle_list             | 4.31 us                                                                      | 4.50 us: 1.04x slower                                                      |
| coroutines              | 22.5 ms                                                                      | 23.7 ms: 1.05x slower                                                      |
| coverage                | 79.0 ms                                                                      | 86.2 ms: 1.09x slower                                                      |
| pickle_dict             | 30.8 us                                                                      | 33.6 us: 1.09x slower                                                      |
| Geometric mean          | (ref)                                                                        | 1.00x slower                                                               |

Benchmark hidden because not significant (41): pickle, bench_mp_pool, django_template, async_tree_memoization_tg, crypto_pyaes, gunicorn, xml_etree_process, async_generators, deltablue, async_tree_cpu_io_mixed_tg, logging_format, nbody, hexiom, async_tree_io, mdp, async_tree_none_tg, docutils, chaos, json, async_tree_cpu_io_mixed, typing_runtime_protocols, meteor_contest, sqlglot_normalize, go, async_tree_io_tg, scimark_fft, async_tree_memoization, mypy2, xml_etree_parse, async_tree_none, logging_simple, html5lib, float, richards_super, sqlglot_optimize, dask, json_dumps, pprint_pformat, tornado_http, regex_v8, telco

# HPT report

- Reliability score: 58.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
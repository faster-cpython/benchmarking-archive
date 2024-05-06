# Results vs. base

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: e20fffa
- commit date: 2024-04-17
- overall geometric mean: 1.00x faster
- HPT reliability: 89.47%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| chameleon      | 6.94 ms                                                                | 7.20 ms: 1.04x slower                                                         |
| docutils       | 2.83 sec                                                               | 2.84 sec: 1.00x slower                                                        |
| tornado_http   | 93.9 ms                                                                | 94.1 ms: 1.00x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                  |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 191 ms: 1.08x faster                                                          |
| nbody          | 90.0 ms                                                                | 85.0 ms: 1.06x faster                                                         |
| float          | 78.7 ms                                                                | 77.2 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 218 ms                                                                 | 221 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                  |

Benchmark hidden because not significant (3): regex_compile, regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 5.33 us                                                                | 4.89 us: 1.09x faster                                                         |
| pickle_dict          | 35.4 us                                                                | 32.7 us: 1.08x faster                                                         |
| unpickle             | 15.2 us                                                                | 14.8 us: 1.03x faster                                                         |
| pickle               | 11.8 us                                                                | 11.6 us: 1.02x faster                                                         |
| json_loads           | 27.6 us                                                                | 27.5 us: 1.00x faster                                                         |
| xml_etree_process    | 60.8 ms                                                                | 61.0 ms: 1.00x slower                                                         |
| unpickle_pure_python | 217 us                                                                 | 219 us: 1.01x slower                                                          |
| xml_etree_iterparse  | 107 ms                                                                 | 108 ms: 1.01x slower                                                          |
| json_dumps           | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| unpickle_list        | 4.99 us                                                                | 5.08 us: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (4): pickle_pure_python, xml_etree_generate, tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.11 ms                                                                | 7.06 ms: 1.01x faster                                                         |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 35.8 ms                                                                | 35.0 ms: 1.02x faster                                                         |
| mako            | 11.1 ms                                                                | 10.9 ms: 1.01x faster                                                         |
| genshi_xml      | 52.1 ms                                                                | 52.9 ms: 1.02x slower                                                         |
| genshi_text     | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                                         |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                                  |

All benchmarks:
===============

| Benchmark               | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list             | 5.33 us                                                                | 4.89 us: 1.09x faster                                                         |
| pidigits                | 206 ms                                                                 | 191 ms: 1.08x faster                                                          |
| pickle_dict             | 35.4 us                                                                | 32.7 us: 1.08x faster                                                         |
| nbody                   | 90.0 ms                                                                | 85.0 ms: 1.06x faster                                                         |
| crypto_pyaes            | 76.3 ms                                                                | 72.9 ms: 1.05x faster                                                         |
| raytrace                | 264 ms                                                                 | 257 ms: 1.03x faster                                                          |
| unpickle                | 15.2 us                                                                | 14.8 us: 1.03x faster                                                         |
| django_template         | 35.8 ms                                                                | 35.0 ms: 1.02x faster                                                         |
| pyflate                 | 471 ms                                                                 | 461 ms: 1.02x faster                                                          |
| float                   | 78.7 ms                                                                | 77.2 ms: 1.02x faster                                                         |
| generators              | 30.9 ms                                                                | 30.4 ms: 1.02x faster                                                         |
| richards                | 47.9 ms                                                                | 47.1 ms: 1.02x faster                                                         |
| pickle                  | 11.8 us                                                                | 11.6 us: 1.02x faster                                                         |
| richards_super          | 53.7 ms                                                                | 52.9 ms: 1.02x faster                                                         |
| deepcopy_reduce         | 3.23 us                                                                | 3.19 us: 1.01x faster                                                         |
| mako                    | 11.1 ms                                                                | 10.9 ms: 1.01x faster                                                         |
| coroutines              | 22.7 ms                                                                | 22.4 ms: 1.01x faster                                                         |
| hexiom                  | 6.43 ms                                                                | 6.35 ms: 1.01x faster                                                         |
| deltablue               | 3.26 ms                                                                | 3.22 ms: 1.01x faster                                                         |
| go                      | 144 ms                                                                 | 143 ms: 1.01x faster                                                          |
| mdp                     | 2.60 sec                                                               | 2.58 sec: 1.01x faster                                                        |
| sqlglot_normalize       | 112 ms                                                                 | 111 ms: 1.01x faster                                                          |
| comprehensions          | 16.9 us                                                                | 16.8 us: 1.01x faster                                                         |
| meteor_contest          | 111 ms                                                                 | 110 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl         | 1.85 sec                                                               | 1.83 sec: 1.01x faster                                                        |
| python_startup_no_site  | 7.11 ms                                                                | 7.06 ms: 1.01x faster                                                         |
| bench_thread_pool       | 841 us                                                                 | 837 us: 1.01x faster                                                          |
| asyncio_tcp             | 507 ms                                                                 | 505 ms: 1.00x faster                                                          |
| dulwich_log             | 66.4 ms                                                                | 66.1 ms: 1.00x faster                                                         |
| json_loads              | 27.6 us                                                                | 27.5 us: 1.00x faster                                                         |
| python_startup          | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                         |
| tornado_http            | 93.9 ms                                                                | 94.1 ms: 1.00x slower                                                         |
| docutils                | 2.83 sec                                                               | 2.84 sec: 1.00x slower                                                        |
| xml_etree_process       | 60.8 ms                                                                | 61.0 ms: 1.00x slower                                                         |
| unpickle_pure_python    | 217 us                                                                 | 219 us: 1.01x slower                                                          |
| sympy_integrate         | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                         |
| xml_etree_iterparse     | 107 ms                                                                 | 108 ms: 1.01x slower                                                          |
| json_dumps              | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| scimark_fft             | 369 ms                                                                 | 374 ms: 1.01x slower                                                          |
| scimark_sparse_mat_mult | 5.20 ms                                                                | 5.26 ms: 1.01x slower                                                         |
| regex_dna               | 218 ms                                                                 | 221 ms: 1.01x slower                                                          |
| genshi_xml              | 52.1 ms                                                                | 52.9 ms: 1.02x slower                                                         |
| scimark_lu              | 117 ms                                                                 | 118 ms: 1.02x slower                                                          |
| pprint_safe_repr        | 754 ms                                                                 | 766 ms: 1.02x slower                                                          |
| deepcopy_memo           | 37.7 us                                                                | 38.4 us: 1.02x slower                                                         |
| telco                   | 8.55 ms                                                                | 8.69 ms: 1.02x slower                                                         |
| scimark_sor             | 123 ms                                                                 | 125 ms: 1.02x slower                                                          |
| unpickle_list           | 4.99 us                                                                | 5.08 us: 1.02x slower                                                         |
| genshi_text             | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                                         |
| pprint_pformat          | 1.53 sec                                                               | 1.57 sec: 1.02x slower                                                        |
| chameleon               | 6.94 ms                                                                | 7.20 ms: 1.04x slower                                                         |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (50): async_tree_io, coverage, html5lib, dask, async_tree_memoization, logging_simple, create_gc_cycles, regex_compile, sqlglot_parse, scimark_monte_carlo, json, logging_silent, async_generators, sqlglot_optimize, thrift, asyncio_websockets, regex_v8, sympy_expand, bench_mp_pool, fannkuch, gunicorn, regex_effbot, typing_runtime_protocols, chaos, async_tree_memoization_tg, pickle_pure_python, pylint, async_tree_none_tg, spectral_norm, async_tree_cpu_io_mixed_tg, aiohttp, sqlite_synth, deepcopy, logging_format, nqueens, 2to3, sqlglot_transpile, sympy_sum, mypy2, async_tree_io_tg, xml_etree_generate, tomli_loads, sympy_str, gc_traversal, pathlib, async_tree_cpu_io_mixed, xml_etree_parse, pycparser, djangocms, async_tree_none

# HPT report

- Reliability score: 89.47% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
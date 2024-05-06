# Results vs. base

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 5032ad9
- commit date: 2024-05-01
- overall geometric mean: 1.00x slower
- HPT reliability: 99.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 271 ms                                                                 | 272 ms: 1.00x slower                                                             |
| chameleon      | 7.09 ms                                                                | 7.26 ms: 1.02x slower                                                            |
| docutils       | 2.80 sec                                                               | 2.82 sec: 1.01x slower                                                           |
| html5lib       | 66.2 ms                                                                | 68.6 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 93.1 ms                                                                | 88.3 ms: 1.05x faster                                                            |
| float          | 78.7 ms                                                                | 77.9 ms: 1.01x faster                                                            |
| pidigits       | 190 ms                                                                 | 191 ms: 1.00x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.82 ms                                                                | 3.89 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (3): regex_dna, regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.24 us                                                                | 5.05 us: 1.04x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                                 | 107 ms: 1.01x faster                                                             |
| unpickle_pure_python | 219 us                                                                 | 217 us: 1.01x faster                                                             |
| unpickle_list        | 5.30 us                                                                | 5.28 us: 1.00x faster                                                            |
| xml_etree_process    | 61.5 ms                                                                | 61.8 ms: 1.00x slower                                                            |
| tomli_loads          | 2.15 sec                                                               | 2.17 sec: 1.01x slower                                                           |
| pickle               | 11.9 us                                                                | 12.0 us: 1.01x slower                                                            |
| json_loads           | 28.1 us                                                                | 28.4 us: 1.01x slower                                                            |
| xml_etree_generate   | 88.2 ms                                                                | 89.0 ms: 1.01x slower                                                            |
| pickle_dict          | 34.3 us                                                                | 34.7 us: 1.01x slower                                                            |
| pickle_pure_python   | 307 us                                                                 | 311 us: 1.01x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (3): unpickle, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                            |
| mako           | 11.2 ms                                                                | 11.5 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody                   | 93.1 ms                                                                | 88.3 ms: 1.05x faster                                                            |
| logging_silent          | 103 ns                                                                 | 98.1 ns: 1.05x faster                                                            |
| coroutines              | 22.9 ms                                                                | 22.0 ms: 1.04x faster                                                            |
| pickle_list             | 5.24 us                                                                | 5.05 us: 1.04x faster                                                            |
| xml_etree_iterparse     | 108 ms                                                                 | 107 ms: 1.01x faster                                                             |
| genshi_text             | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                            |
| hexiom                  | 6.22 ms                                                                | 6.16 ms: 1.01x faster                                                            |
| comprehensions          | 16.6 us                                                                | 16.4 us: 1.01x faster                                                            |
| unpickle_pure_python    | 219 us                                                                 | 217 us: 1.01x faster                                                             |
| float                   | 78.7 ms                                                                | 77.9 ms: 1.01x faster                                                            |
| pyflate                 | 484 ms                                                                 | 480 ms: 1.01x faster                                                             |
| dulwich_log             | 66.1 ms                                                                | 65.6 ms: 1.01x faster                                                            |
| sympy_str               | 280 ms                                                                 | 278 ms: 1.01x faster                                                             |
| create_gc_cycles        | 1.76 ms                                                                | 1.75 ms: 1.01x faster                                                            |
| chaos                   | 61.0 ms                                                                | 60.6 ms: 1.01x faster                                                            |
| pathlib                 | 17.7 ms                                                                | 17.6 ms: 1.01x faster                                                            |
| asyncio_tcp_ssl         | 1.84 sec                                                               | 1.84 sec: 1.00x faster                                                           |
| unpickle_list           | 5.30 us                                                                | 5.28 us: 1.00x faster                                                            |
| python_startup          | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| sympy_integrate         | 20.3 ms                                                                | 20.3 ms: 1.00x slower                                                            |
| 2to3                    | 271 ms                                                                 | 272 ms: 1.00x slower                                                             |
| sympy_expand            | 468 ms                                                                 | 470 ms: 1.00x slower                                                             |
| sqlglot_transpile       | 1.59 ms                                                                | 1.60 ms: 1.00x slower                                                            |
| pidigits                | 190 ms                                                                 | 191 ms: 1.00x slower                                                             |
| scimark_sor             | 130 ms                                                                 | 131 ms: 1.00x slower                                                             |
| xml_etree_process       | 61.5 ms                                                                | 61.8 ms: 1.00x slower                                                            |
| raytrace                | 265 ms                                                                 | 267 ms: 1.01x slower                                                             |
| sympy_sum               | 154 ms                                                                 | 155 ms: 1.01x slower                                                             |
| deltablue               | 3.20 ms                                                                | 3.22 ms: 1.01x slower                                                            |
| async_generators        | 443 ms                                                                 | 445 ms: 1.01x slower                                                             |
| sqlglot_parse           | 1.29 ms                                                                | 1.29 ms: 1.01x slower                                                            |
| tomli_loads             | 2.15 sec                                                               | 2.17 sec: 1.01x slower                                                           |
| pickle                  | 11.9 us                                                                | 12.0 us: 1.01x slower                                                            |
| logging_format          | 6.35 us                                                                | 6.39 us: 1.01x slower                                                            |
| docutils                | 2.80 sec                                                               | 2.82 sec: 1.01x slower                                                           |
| json_loads              | 28.1 us                                                                | 28.4 us: 1.01x slower                                                            |
| richards_super          | 54.2 ms                                                                | 54.6 ms: 1.01x slower                                                            |
| asyncio_tcp             | 507 ms                                                                 | 511 ms: 1.01x slower                                                             |
| xml_etree_generate      | 88.2 ms                                                                | 89.0 ms: 1.01x slower                                                            |
| pickle_dict             | 34.3 us                                                                | 34.7 us: 1.01x slower                                                            |
| pprint_safe_repr        | 750 ms                                                                 | 758 ms: 1.01x slower                                                             |
| scimark_sparse_mat_mult | 5.15 ms                                                                | 5.21 ms: 1.01x slower                                                            |
| pickle_pure_python      | 307 us                                                                 | 311 us: 1.01x slower                                                             |
| richards                | 47.6 ms                                                                | 48.3 ms: 1.01x slower                                                            |
| logging_simple          | 5.71 us                                                                | 5.80 us: 1.01x slower                                                            |
| pprint_pformat          | 1.53 sec                                                               | 1.55 sec: 1.02x slower                                                           |
| deepcopy_memo           | 37.4 us                                                                | 38.0 us: 1.02x slower                                                            |
| deepcopy                | 355 us                                                                 | 361 us: 1.02x slower                                                             |
| meteor_contest          | 109 ms                                                                 | 111 ms: 1.02x slower                                                             |
| regex_effbot            | 3.82 ms                                                                | 3.89 ms: 1.02x slower                                                            |
| spectral_norm           | 108 ms                                                                 | 110 ms: 1.02x slower                                                             |
| chameleon               | 7.09 ms                                                                | 7.26 ms: 1.02x slower                                                            |
| crypto_pyaes            | 73.7 ms                                                                | 75.6 ms: 1.03x slower                                                            |
| mako                    | 11.2 ms                                                                | 11.5 ms: 1.03x slower                                                            |
| scimark_monte_carlo     | 68.7 ms                                                                | 70.5 ms: 1.03x slower                                                            |
| scimark_fft             | 367 ms                                                                 | 377 ms: 1.03x slower                                                             |
| scimark_lu              | 114 ms                                                                 | 118 ms: 1.03x slower                                                             |
| fannkuch                | 392 ms                                                                 | 403 ms: 1.03x slower                                                             |
| html5lib                | 66.2 ms                                                                | 68.6 ms: 1.04x slower                                                            |
| json                    | 5.15 ms                                                                | 5.37 ms: 1.04x slower                                                            |
| gc_traversal            | 3.80 ms                                                                | 3.98 ms: 1.05x slower                                                            |
| mdp                     | 2.57 sec                                                               | 2.72 sec: 1.06x slower                                                           |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (39): unpickle, xml_etree_parse, django_template, deepcopy_reduce, dask, async_tree_io_tg, thrift, tornado_http, async_tree_io, sqlite_synth, coverage, aiohttp, go, genshi_xml, sqlglot_optimize, regex_dna, sqlglot_normalize, telco, regex_v8, bench_thread_pool, python_startup_no_site, generators, asyncio_websockets, async_tree_memoization_tg, bench_mp_pool, nqueens, regex_compile, json_dumps, gunicorn, typing_runtime_protocols, mypy2, async_tree_none_tg, async_tree_none, pylint, async_tree_cpu_io_mixed, pycparser, async_tree_memoization, async_tree_cpu_io_mixed_tg, djangocms

# HPT report

- Reliability score: 99.43% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
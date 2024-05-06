# Results vs. base

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: dedffa7
- commit date: 2024-05-01
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 271 ms                                                                 | 272 ms: 1.00x slower                                                             |
| chameleon      | 7.09 ms                                                                | 7.41 ms: 1.05x slower                                                            |
| docutils       | 2.80 sec                                                               | 2.81 sec: 1.00x slower                                                           |
| html5lib       | 66.2 ms                                                                | 68.2 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_none, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 93.1 ms                                                                | 88.4 ms: 1.05x faster                                                            |
| float          | 78.7 ms                                                                | 79.1 ms: 1.01x slower                                                            |
| pidigits       | 190 ms                                                                 | 195 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.82 ms                                                                | 3.71 ms: 1.03x faster                                                            |
| regex_dna      | 231 ms                                                                 | 225 ms: 1.02x faster                                                             |
| regex_v8       | 25.8 ms                                                                | 25.6 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle             | 15.5 us                                                                | 15.1 us: 1.03x faster                                                            |
| pickle               | 11.9 us                                                                | 11.6 us: 1.03x faster                                                            |
| pickle_list          | 5.24 us                                                                | 5.12 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                                 | 107 ms: 1.01x faster                                                             |
| unpickle_pure_python | 219 us                                                                 | 221 us: 1.01x slower                                                             |
| json_loads           | 28.1 us                                                                | 28.4 us: 1.01x slower                                                            |
| unpickle_list        | 5.30 us                                                                | 5.35 us: 1.01x slower                                                            |
| pickle_pure_python   | 307 us                                                                 | 311 us: 1.01x slower                                                             |
| xml_etree_process    | 61.5 ms                                                                | 62.3 ms: 1.01x slower                                                            |
| xml_etree_generate   | 88.2 ms                                                                | 90.3 ms: 1.02x slower                                                            |
| pickle_dict          | 34.3 us                                                                | 35.9 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (3): xml_etree_parse, json_dumps, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site | 7.09 ms                                                                | 7.08 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.8 ms                                                                | 35.1 ms: 1.01x slower                                                            |
| mako            | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                                            |
| genshi_text     | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark              | bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6+-21c09d9 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody                  | 93.1 ms                                                                | 88.4 ms: 1.05x faster                                                            |
| unpickle               | 15.5 us                                                                | 15.1 us: 1.03x faster                                                            |
| regex_effbot           | 3.82 ms                                                                | 3.71 ms: 1.03x faster                                                            |
| pickle                 | 11.9 us                                                                | 11.6 us: 1.03x faster                                                            |
| regex_dna              | 231 ms                                                                 | 225 ms: 1.02x faster                                                             |
| pickle_list            | 5.24 us                                                                | 5.12 us: 1.02x faster                                                            |
| xml_etree_iterparse    | 108 ms                                                                 | 107 ms: 1.01x faster                                                             |
| chaos                  | 61.0 ms                                                                | 60.6 ms: 1.01x faster                                                            |
| pathlib                | 17.7 ms                                                                | 17.5 ms: 1.01x faster                                                            |
| regex_v8               | 25.8 ms                                                                | 25.6 ms: 1.01x faster                                                            |
| comprehensions         | 16.6 us                                                                | 16.5 us: 1.01x faster                                                            |
| coroutines             | 22.9 ms                                                                | 22.8 ms: 1.01x faster                                                            |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| create_gc_cycles       | 1.76 ms                                                                | 1.75 ms: 1.00x faster                                                            |
| python_startup_no_site | 7.09 ms                                                                | 7.08 ms: 1.00x faster                                                            |
| bench_thread_pool      | 824 us                                                                 | 826 us: 1.00x slower                                                             |
| asyncio_tcp            | 507 ms                                                                 | 508 ms: 1.00x slower                                                             |
| sqlglot_optimize       | 55.0 ms                                                                | 55.2 ms: 1.00x slower                                                            |
| 2to3                   | 271 ms                                                                 | 272 ms: 1.00x slower                                                             |
| async_generators       | 443 ms                                                                 | 445 ms: 1.00x slower                                                             |
| docutils               | 2.80 sec                                                               | 2.81 sec: 1.00x slower                                                           |
| sqlglot_normalize      | 110 ms                                                                 | 110 ms: 1.00x slower                                                             |
| float                  | 78.7 ms                                                                | 79.1 ms: 1.01x slower                                                            |
| thrift                 | 816 us                                                                 | 822 us: 1.01x slower                                                             |
| sympy_expand           | 468 ms                                                                 | 472 ms: 1.01x slower                                                             |
| django_template        | 34.8 ms                                                                | 35.1 ms: 1.01x slower                                                            |
| sympy_integrate        | 20.3 ms                                                                | 20.4 ms: 1.01x slower                                                            |
| unpickle_pure_python   | 219 us                                                                 | 221 us: 1.01x slower                                                             |
| json_loads             | 28.1 us                                                                | 28.4 us: 1.01x slower                                                            |
| sympy_sum              | 154 ms                                                                 | 155 ms: 1.01x slower                                                             |
| unpickle_list          | 5.30 us                                                                | 5.35 us: 1.01x slower                                                            |
| pyflate                | 484 ms                                                                 | 489 ms: 1.01x slower                                                             |
| deltablue              | 3.20 ms                                                                | 3.23 ms: 1.01x slower                                                            |
| sqlglot_parse          | 1.29 ms                                                                | 1.30 ms: 1.01x slower                                                            |
| logging_format         | 6.35 us                                                                | 6.42 us: 1.01x slower                                                            |
| go                     | 144 ms                                                                 | 146 ms: 1.01x slower                                                             |
| sqlglot_transpile      | 1.59 ms                                                                | 1.61 ms: 1.01x slower                                                            |
| pickle_pure_python     | 307 us                                                                 | 311 us: 1.01x slower                                                             |
| xml_etree_process      | 61.5 ms                                                                | 62.3 ms: 1.01x slower                                                            |
| logging_simple         | 5.71 us                                                                | 5.79 us: 1.01x slower                                                            |
| mako                   | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                                            |
| genshi_text            | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                            |
| pprint_safe_repr       | 750 ms                                                                 | 761 ms: 1.02x slower                                                             |
| hexiom                 | 6.22 ms                                                                | 6.33 ms: 1.02x slower                                                            |
| pprint_pformat         | 1.53 sec                                                               | 1.56 sec: 1.02x slower                                                           |
| scimark_monte_carlo    | 68.7 ms                                                                | 70.0 ms: 1.02x slower                                                            |
| xml_etree_generate     | 88.2 ms                                                                | 90.3 ms: 1.02x slower                                                            |
| meteor_contest         | 109 ms                                                                 | 111 ms: 1.02x slower                                                             |
| deepcopy               | 355 us                                                                 | 364 us: 1.02x slower                                                             |
| crypto_pyaes           | 73.7 ms                                                                | 75.6 ms: 1.03x slower                                                            |
| fannkuch               | 392 ms                                                                 | 402 ms: 1.03x slower                                                             |
| richards_super         | 54.2 ms                                                                | 55.6 ms: 1.03x slower                                                            |
| scimark_sor            | 130 ms                                                                 | 134 ms: 1.03x slower                                                             |
| pidigits               | 190 ms                                                                 | 195 ms: 1.03x slower                                                             |
| scimark_fft            | 367 ms                                                                 | 377 ms: 1.03x slower                                                             |
| logging_silent         | 103 ns                                                                 | 106 ns: 1.03x slower                                                             |
| scimark_lu             | 114 ms                                                                 | 118 ms: 1.03x slower                                                             |
| richards               | 47.6 ms                                                                | 49.0 ms: 1.03x slower                                                            |
| html5lib               | 66.2 ms                                                                | 68.2 ms: 1.03x slower                                                            |
| deepcopy_memo          | 37.4 us                                                                | 38.7 us: 1.03x slower                                                            |
| spectral_norm          | 108 ms                                                                 | 111 ms: 1.03x slower                                                             |
| chameleon              | 7.09 ms                                                                | 7.41 ms: 1.05x slower                                                            |
| pickle_dict            | 34.3 us                                                                | 35.9 us: 1.05x slower                                                            |
| gc_traversal           | 3.80 ms                                                                | 3.98 ms: 1.05x slower                                                            |
| json                   | 5.15 ms                                                                | 5.53 ms: 1.07x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (36): async_tree_memoization, xml_etree_parse, djangocms, sqlite_synth, dask, dulwich_log, genshi_xml, deepcopy_reduce, telco, gunicorn, mdp, asyncio_tcp_ssl, bench_mp_pool, tornado_http, aiohttp, json_dumps, regex_compile, raytrace, asyncio_websockets, nqueens, async_tree_none, generators, tomli_loads, mypy2, sympy_str, pylint, async_tree_memoization_tg, typing_runtime_protocols, async_tree_io, coverage, async_tree_cpu_io_mixed, scimark_sparse_mat_mult, pycparser, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
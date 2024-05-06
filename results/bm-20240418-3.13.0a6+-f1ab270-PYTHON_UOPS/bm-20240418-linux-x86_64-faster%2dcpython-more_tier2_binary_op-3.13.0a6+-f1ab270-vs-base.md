# Results vs. base

- fork: faster-cpython
- ref: more_tier2_binary_op
- machine: linux-x86_64
- commit hash: f1ab270
- commit date: 2024-04-18
- overall geometric mean: 1.01x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6+-e32f6e9 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 333 ms                                                                 | 330 ms: 1.01x faster                                                             |
| html5lib       | 75.3 ms                                                                | 73.7 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_none, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6+-e32f6e9 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 138 ms                                                                 | 135 ms: 1.03x faster                                                             |
| nbody          | 213 ms                                                                 | 209 ms: 1.02x faster                                                             |
| pidigits       | 194 ms                                                                 | 202 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6+-e32f6e9 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.91 ms                                                                | 3.61 ms: 1.08x faster                                                            |
| regex_dna      | 235 ms                                                                 | 226 ms: 1.04x faster                                                             |
| regex_v8       | 26.8 ms                                                                | 25.8 ms: 1.04x faster                                                            |
| regex_compile  | 224 ms                                                                 | 220 ms: 1.02x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6+-e32f6e9 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.27 us                                                                | 4.97 us: 1.06x faster                                                            |
| pickle               | 12.0 us                                                                | 11.7 us: 1.02x faster                                                            |
| unpickle_pure_python | 410 us                                                                 | 404 us: 1.01x faster                                                             |
| tomli_loads          | 3.56 sec                                                               | 3.52 sec: 1.01x faster                                                           |
| pickle_dict          | 34.5 us                                                                | 34.4 us: 1.00x faster                                                            |
| json_loads           | 27.6 us                                                                | 27.9 us: 1.01x slower                                                            |
| unpickle_list        | 4.97 us                                                                | 5.08 us: 1.02x slower                                                            |
| unpickle             | 16.1 us                                                                | 17.0 us: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (6): xml_etree_generate, xml_etree_iterparse, xml_etree_process, pickle_pure_python, json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6+-e32f6e9 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 65.1 ms                                                                | 64.0 ms: 1.02x faster                                                            |
| mako           | 21.3 ms                                                                | 21.1 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark               | bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6+-e32f6e9 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot            | 3.91 ms                                                                | 3.61 ms: 1.08x faster                                                            |
| pickle_list             | 5.27 us                                                                | 4.97 us: 1.06x faster                                                            |
| regex_dna               | 235 ms                                                                 | 226 ms: 1.04x faster                                                             |
| regex_v8                | 26.8 ms                                                                | 25.8 ms: 1.04x faster                                                            |
| spectral_norm           | 250 ms                                                                 | 242 ms: 1.03x faster                                                             |
| scimark_sparse_mat_mult | 9.29 ms                                                                | 9.00 ms: 1.03x faster                                                            |
| pycparser               | 1.39 sec                                                               | 1.35 sec: 1.03x faster                                                           |
| float                   | 138 ms                                                                 | 135 ms: 1.03x faster                                                             |
| pickle                  | 12.0 us                                                                | 11.7 us: 1.02x faster                                                            |
| scimark_monte_carlo     | 143 ms                                                                 | 139 ms: 1.02x faster                                                             |
| html5lib                | 75.3 ms                                                                | 73.7 ms: 1.02x faster                                                            |
| nbody                   | 213 ms                                                                 | 209 ms: 1.02x faster                                                             |
| hexiom                  | 15.4 ms                                                                | 15.1 ms: 1.02x faster                                                            |
| genshi_xml              | 65.1 ms                                                                | 64.0 ms: 1.02x faster                                                            |
| regex_compile           | 224 ms                                                                 | 220 ms: 1.02x faster                                                             |
| scimark_lu              | 211 ms                                                                 | 208 ms: 1.02x faster                                                             |
| richards_super          | 82.9 ms                                                                | 81.6 ms: 1.02x faster                                                            |
| coroutines              | 22.9 ms                                                                | 22.5 ms: 1.02x faster                                                            |
| richards                | 76.3 ms                                                                | 75.2 ms: 1.01x faster                                                            |
| pprint_safe_repr        | 1.27 sec                                                               | 1.25 sec: 1.01x faster                                                           |
| pyflate                 | 890 ms                                                                 | 878 ms: 1.01x faster                                                             |
| scimark_fft             | 642 ms                                                                 | 633 ms: 1.01x faster                                                             |
| unpickle_pure_python    | 410 us                                                                 | 404 us: 1.01x faster                                                             |
| logging_simple          | 6.66 us                                                                | 6.58 us: 1.01x faster                                                            |
| pprint_pformat          | 2.64 sec                                                               | 2.60 sec: 1.01x faster                                                           |
| json                    | 5.22 ms                                                                | 5.16 ms: 1.01x faster                                                            |
| tomli_loads             | 3.56 sec                                                               | 3.52 sec: 1.01x faster                                                           |
| fannkuch                | 773 ms                                                                 | 764 ms: 1.01x faster                                                             |
| logging_silent          | 110 ns                                                                 | 109 ns: 1.01x faster                                                             |
| sqlglot_transpile       | 2.00 ms                                                                | 1.97 ms: 1.01x faster                                                            |
| 2to3                    | 333 ms                                                                 | 330 ms: 1.01x faster                                                             |
| coverage                | 99.5 ms                                                                | 98.5 ms: 1.01x faster                                                            |
| thrift                  | 843 us                                                                 | 836 us: 1.01x faster                                                             |
| sqlglot_parse           | 1.65 ms                                                                | 1.63 ms: 1.01x faster                                                            |
| bench_thread_pool       | 935 us                                                                 | 928 us: 1.01x faster                                                             |
| mako                    | 21.3 ms                                                                | 21.1 ms: 1.01x faster                                                            |
| sympy_str               | 350 ms                                                                 | 347 ms: 1.01x faster                                                             |
| mdp                     | 3.03 sec                                                               | 3.01 sec: 1.01x faster                                                           |
| gunicorn                | 1.35 ms                                                                | 1.34 ms: 1.01x faster                                                            |
| go                      | 230 ms                                                                 | 229 ms: 1.01x faster                                                             |
| crypto_pyaes            | 129 ms                                                                 | 128 ms: 1.01x faster                                                             |
| sympy_integrate         | 25.5 ms                                                                | 25.3 ms: 1.00x faster                                                            |
| pickle_dict             | 34.5 us                                                                | 34.4 us: 1.00x faster                                                            |
| asyncio_tcp             | 516 ms                                                                 | 514 ms: 1.00x faster                                                             |
| deepcopy_memo           | 50.1 us                                                                | 49.9 us: 1.00x faster                                                            |
| asyncio_tcp_ssl         | 1.86 sec                                                               | 1.87 sec: 1.00x slower                                                           |
| dulwich_log             | 75.5 ms                                                                | 75.8 ms: 1.00x slower                                                            |
| sqlglot_normalize       | 133 ms                                                                 | 133 ms: 1.01x slower                                                             |
| raytrace                | 376 ms                                                                 | 378 ms: 1.01x slower                                                             |
| create_gc_cycles        | 1.78 ms                                                                | 1.79 ms: 1.01x slower                                                            |
| pathlib                 | 18.4 ms                                                                | 18.5 ms: 1.01x slower                                                            |
| deepcopy                | 392 us                                                                 | 395 us: 1.01x slower                                                             |
| json_loads              | 27.6 us                                                                | 27.9 us: 1.01x slower                                                            |
| telco                   | 9.65 ms                                                                | 9.78 ms: 1.01x slower                                                            |
| unpickle_list           | 4.97 us                                                                | 5.08 us: 1.02x slower                                                            |
| pidigits                | 194 ms                                                                 | 202 ms: 1.04x slower                                                             |
| unpickle                | 16.1 us                                                                | 17.0 us: 1.06x slower                                                            |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (44): djangocms, asyncio_websockets, async_tree_io, async_tree_none, nqueens, genshi_text, mypy2, scimark_sor, docutils, chaos, xml_etree_generate, sqlglot_optimize, xml_etree_iterparse, async_tree_none_tg, sympy_sum, sqlite_synth, generators, xml_etree_process, python_startup, async_tree_memoization, tornado_http, pickle_pure_python, pylint, json_dumps, python_startup_no_site, bench_mp_pool, gc_traversal, sympy_expand, async_generators, aiohttp, meteor_contest, chameleon, async_tree_io_tg, dask, django_template, logging_format, comprehensions, async_tree_memoization_tg, deltablue, deepcopy_reduce, async_tree_cpu_io_mixed, typing_runtime_protocols, xml_etree_parse, async_tree_cpu_io_mixed_tg

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
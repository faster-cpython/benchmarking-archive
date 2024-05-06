# Results vs. base

- fork: python
- ref: c408c36e9b346f9f15a3
- machine: linux-aarch64
- commit hash: c408c36
- commit date: 2024-05-01
- overall geometric mean: 1.00x slower
- HPT reliability: 80.56%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| chameleon      | 9.13 ms                                                  | 9.37 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 90.3 ms                                                  | 89.2 ms: 1.01x faster                                                    |
| nbody          | 108 ms                                                   | 107 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 30.3 ms                                                  | 30.2 ms: 1.00x faster                                                    |
| regex_effbot   | 4.84 ms                                                  | 4.85 ms: 1.00x slower                                                    |
| regex_dna      | 246 ms                                                   | 247 ms: 1.00x slower                                                     |
| regex_compile  | 159 ms                                                   | 160 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_list        | 6.48 us                                                  | 6.31 us: 1.03x faster                                                    |
| xml_etree_iterparse  | 148 ms                                                   | 147 ms: 1.01x faster                                                     |
| pickle               | 13.5 us                                                  | 13.4 us: 1.01x faster                                                    |
| pickle_pure_python   | 356 us                                                   | 354 us: 1.01x faster                                                     |
| pickle_list          | 5.26 us                                                  | 5.23 us: 1.01x faster                                                    |
| unpickle_pure_python | 277 us                                                   | 276 us: 1.00x faster                                                     |
| json_dumps           | 12.9 ms                                                  | 12.8 ms: 1.00x faster                                                    |
| unpickle             | 19.8 us                                                  | 19.7 us: 1.00x faster                                                    |
| tomli_loads          | 2.56 sec                                                 | 2.57 sec: 1.00x slower                                                   |
| xml_etree_parse      | 186 ms                                                   | 188 ms: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (4): xml_etree_generate, xml_etree_process, pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 13.0 ms                                                  | 12.8 ms: 1.01x faster                                                    |
| django_template | 48.5 ms                                                  | 48.3 ms: 1.01x faster                                                    |
| genshi_text     | 33.6 ms                                                  | 33.8 ms: 1.00x slower                                                    |
| genshi_xml      | 78.3 ms                                                  | 79.5 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|--------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_list            | 6.48 us                                                  | 6.31 us: 1.03x faster                                                    |
| mako                     | 13.0 ms                                                  | 12.8 ms: 1.01x faster                                                    |
| float                    | 90.3 ms                                                  | 89.2 ms: 1.01x faster                                                    |
| sqlite_synth             | 3.85 us                                                  | 3.81 us: 1.01x faster                                                    |
| typing_runtime_protocols | 215 us                                                   | 213 us: 1.01x faster                                                     |
| pyflate                  | 598 ms                                                   | 592 ms: 1.01x faster                                                     |
| meteor_contest           | 120 ms                                                   | 119 ms: 1.01x faster                                                     |
| chaos                    | 82.8 ms                                                  | 82.1 ms: 1.01x faster                                                    |
| xml_etree_iterparse      | 148 ms                                                   | 147 ms: 1.01x faster                                                     |
| pickle                   | 13.5 us                                                  | 13.4 us: 1.01x faster                                                    |
| pickle_pure_python       | 356 us                                                   | 354 us: 1.01x faster                                                     |
| pickle_list              | 5.26 us                                                  | 5.23 us: 1.01x faster                                                    |
| scimark_monte_carlo      | 84.8 ms                                                  | 84.4 ms: 1.01x faster                                                    |
| django_template          | 48.5 ms                                                  | 48.3 ms: 1.01x faster                                                    |
| logging_simple           | 7.65 us                                                  | 7.61 us: 1.01x faster                                                    |
| unpickle_pure_python     | 277 us                                                   | 276 us: 1.00x faster                                                     |
| nbody                    | 108 ms                                                   | 107 ms: 1.00x faster                                                     |
| json_dumps               | 12.9 ms                                                  | 12.8 ms: 1.00x faster                                                    |
| unpickle                 | 19.8 us                                                  | 19.7 us: 1.00x faster                                                    |
| mdp                      | 3.44 sec                                                 | 3.43 sec: 1.00x faster                                                   |
| coroutines               | 30.0 ms                                                  | 29.9 ms: 1.00x faster                                                    |
| regex_v8                 | 30.3 ms                                                  | 30.2 ms: 1.00x faster                                                    |
| regex_effbot             | 4.84 ms                                                  | 4.85 ms: 1.00x slower                                                    |
| deepcopy                 | 460 us                                                   | 461 us: 1.00x slower                                                     |
| go                       | 186 ms                                                   | 187 ms: 1.00x slower                                                     |
| regex_dna                | 246 ms                                                   | 247 ms: 1.00x slower                                                     |
| comprehensions           | 23.4 us                                                  | 23.5 us: 1.00x slower                                                    |
| richards                 | 52.3 ms                                                  | 52.5 ms: 1.00x slower                                                    |
| tomli_loads              | 2.56 sec                                                 | 2.57 sec: 1.00x slower                                                   |
| spectral_norm            | 142 ms                                                   | 143 ms: 1.00x slower                                                     |
| genshi_text              | 33.6 ms                                                  | 33.8 ms: 1.00x slower                                                    |
| sympy_str                | 306 ms                                                   | 307 ms: 1.01x slower                                                     |
| regex_compile            | 159 ms                                                   | 160 ms: 1.01x slower                                                     |
| logging_format           | 8.27 us                                                  | 8.34 us: 1.01x slower                                                    |
| xml_etree_parse          | 186 ms                                                   | 188 ms: 1.01x slower                                                     |
| deepcopy_memo            | 50.3 us                                                  | 50.8 us: 1.01x slower                                                    |
| scimark_sor              | 181 ms                                                   | 183 ms: 1.01x slower                                                     |
| bench_thread_pool        | 1.31 ms                                                  | 1.33 ms: 1.01x slower                                                    |
| json                     | 5.59 ms                                                  | 5.66 ms: 1.01x slower                                                    |
| asyncio_tcp              | 614 ms                                                   | 622 ms: 1.01x slower                                                     |
| thrift                   | 971 us                                                   | 985 us: 1.01x slower                                                     |
| genshi_xml               | 78.3 ms                                                  | 79.5 ms: 1.02x slower                                                    |
| scimark_lu               | 178 ms                                                   | 181 ms: 1.02x slower                                                     |
| async_generators         | 501 ms                                                   | 510 ms: 1.02x slower                                                     |
| chameleon                | 9.13 ms                                                  | 9.37 ms: 1.03x slower                                                    |
| deepcopy_reduce          | 4.11 us                                                  | 4.22 us: 1.03x slower                                                    |
| telco                    | 9.88 ms                                                  | 10.3 ms: 1.04x slower                                                    |
| bench_mp_pool            | 7.46 ms                                                  | 8.69 ms: 1.16x slower                                                    |
| Geometric mean           | (ref)                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (49): scimark_sparse_mat_mult, dask, async_tree_cpu_io_mixed, async_tree_none_tg, create_gc_cycles, docutils, sqlglot_parse, async_tree_memoization_tg, async_tree_none, xml_etree_generate, sympy_sum, dulwich_log, async_tree_memoization, scimark_fft, async_tree_cpu_io_mixed_tg, sqlglot_normalize, logging_silent, sqlglot_optimize, richards_super, pycparser, sqlglot_transpile, asyncio_websockets, generators, coverage, xml_etree_process, python_startup, gc_traversal, pidigits, 2to3, hexiom, sympy_integrate, pickle_dict, async_tree_io_tg, raytrace, json_loads, pathlib, python_startup_no_site, deltablue, nqueens, html5lib, sympy_expand, pprint_pformat, crypto_pyaes, fannkuch, asyncio_tcp_ssl, pylint, pprint_safe_repr, tornado_http, async_tree_io

# HPT report

- Reliability score: 80.56% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 278 ms                                                                 | 281 ms: 1.01x slower                                                     |
| chameleon      | 7.11 ms                                                                | 6.90 ms: 1.03x faster                                                    |
| docutils       | 2.92 sec                                                               | 2.97 sec: 1.02x slower                                                   |
| html5lib       | 69.1 ms                                                                | 68.6 ms: 1.01x faster                                                    |
| tornado_http   | 96.1 ms                                                                | 97.2 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_io, async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 189 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.90 ms                                                                | 3.70 ms: 1.05x faster                                                    |
| regex_dna      | 233 ms                                                                 | 223 ms: 1.04x faster                                                     |
| regex_v8       | 26.0 ms                                                                | 25.5 ms: 1.02x faster                                                    |
| regex_compile  | 143 ms                                                                 | 145 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|---------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python  | 310 us                                                                 | 305 us: 1.02x faster                                                     |
| pickle_list         | 4.97 us                                                                | 4.90 us: 1.01x faster                                                    |
| json_loads          | 28.4 us                                                                | 28.1 us: 1.01x faster                                                    |
| xml_etree_generate  | 87.4 ms                                                                | 87.8 ms: 1.00x slower                                                    |
| tomli_loads         | 2.05 sec                                                               | 2.06 sec: 1.01x slower                                                   |
| pickle_dict         | 33.9 us                                                                | 34.2 us: 1.01x slower                                                    |
| pickle              | 11.6 us                                                                | 11.6 us: 1.01x slower                                                    |
| xml_etree_iterparse | 107 ms                                                                 | 107 ms: 1.01x slower                                                     |
| json_dumps          | 10.3 ms                                                                | 10.5 ms: 1.01x slower                                                    |
| unpickle_list       | 5.17 us                                                                | 5.32 us: 1.03x slower                                                    |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (4): unpickle, xml_etree_process, unpickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                                    |
| python_startup_no_site | 9.50 ms                                                                | 9.57 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 10.7 ms                                                                | 10.6 ms: 1.00x faster                                                    |
| genshi_text    | 23.9 ms                                                                | 24.7 ms: 1.03x slower                                                    |
| genshi_xml     | 52.6 ms                                                                | 55.4 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                | bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal             | 3.95 ms                                                                | 3.61 ms: 1.10x faster                                                    |
| regex_effbot             | 3.90 ms                                                                | 3.70 ms: 1.05x faster                                                    |
| regex_dna                | 233 ms                                                                 | 223 ms: 1.04x faster                                                     |
| pidigits                 | 197 ms                                                                 | 189 ms: 1.04x faster                                                     |
| chameleon                | 7.11 ms                                                                | 6.90 ms: 1.03x faster                                                    |
| go                       | 154 ms                                                                 | 149 ms: 1.03x faster                                                     |
| scimark_monte_carlo      | 69.7 ms                                                                | 68.2 ms: 1.02x faster                                                    |
| logging_silent           | 104 ns                                                                 | 101 ns: 1.02x faster                                                     |
| regex_v8                 | 26.0 ms                                                                | 25.5 ms: 1.02x faster                                                    |
| spectral_norm            | 115 ms                                                                 | 113 ms: 1.02x faster                                                     |
| pickle_pure_python       | 310 us                                                                 | 305 us: 1.02x faster                                                     |
| pickle_list              | 4.97 us                                                                | 4.90 us: 1.01x faster                                                    |
| json_loads               | 28.4 us                                                                | 28.1 us: 1.01x faster                                                    |
| html5lib                 | 69.1 ms                                                                | 68.6 ms: 1.01x faster                                                    |
| scimark_fft              | 339 ms                                                                 | 337 ms: 1.00x faster                                                     |
| mako                     | 10.7 ms                                                                | 10.6 ms: 1.00x faster                                                    |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                   |
| async_generators         | 462 ms                                                                 | 464 ms: 1.00x slower                                                     |
| xml_etree_generate       | 87.4 ms                                                                | 87.8 ms: 1.00x slower                                                    |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                                    |
| create_gc_cycles         | 1.75 ms                                                                | 1.76 ms: 1.01x slower                                                    |
| tomli_loads              | 2.05 sec                                                               | 2.06 sec: 1.01x slower                                                   |
| generators               | 29.9 ms                                                                | 30.1 ms: 1.01x slower                                                    |
| pickle_dict              | 33.9 us                                                                | 34.2 us: 1.01x slower                                                    |
| pickle                   | 11.6 us                                                                | 11.6 us: 1.01x slower                                                    |
| python_startup_no_site   | 9.50 ms                                                                | 9.57 ms: 1.01x slower                                                    |
| logging_simple           | 5.89 us                                                                | 5.93 us: 1.01x slower                                                    |
| xml_etree_iterparse      | 107 ms                                                                 | 107 ms: 1.01x slower                                                     |
| sympy_str                | 297 ms                                                                 | 300 ms: 1.01x slower                                                     |
| sqlglot_transpile        | 1.64 ms                                                                | 1.65 ms: 1.01x slower                                                    |
| bench_thread_pool        | 855 us                                                                 | 864 us: 1.01x slower                                                     |
| richards_super           | 49.2 ms                                                                | 49.7 ms: 1.01x slower                                                    |
| aiohttp                  | 1.20 ms                                                                | 1.21 ms: 1.01x slower                                                    |
| json_dumps               | 10.3 ms                                                                | 10.5 ms: 1.01x slower                                                    |
| tornado_http             | 96.1 ms                                                                | 97.2 ms: 1.01x slower                                                    |
| coverage                 | 97.9 ms                                                                | 99.0 ms: 1.01x slower                                                    |
| 2to3                     | 278 ms                                                                 | 281 ms: 1.01x slower                                                     |
| regex_compile            | 143 ms                                                                 | 145 ms: 1.01x slower                                                     |
| deepcopy_reduce          | 3.23 us                                                                | 3.27 us: 1.01x slower                                                    |
| deepcopy                 | 365 us                                                                 | 370 us: 1.01x slower                                                     |
| crypto_pyaes             | 75.0 ms                                                                | 76.0 ms: 1.01x slower                                                    |
| chaos                    | 62.3 ms                                                                | 63.1 ms: 1.01x slower                                                    |
| meteor_contest           | 111 ms                                                                 | 113 ms: 1.01x slower                                                     |
| sqlglot_normalize        | 113 ms                                                                 | 115 ms: 1.01x slower                                                     |
| sympy_expand             | 497 ms                                                                 | 504 ms: 1.02x slower                                                     |
| pyflate                  | 471 ms                                                                 | 478 ms: 1.02x slower                                                     |
| pathlib                  | 19.2 ms                                                                | 19.5 ms: 1.02x slower                                                    |
| mdp                      | 2.62 sec                                                               | 2.66 sec: 1.02x slower                                                   |
| sqlglot_optimize         | 57.2 ms                                                                | 58.1 ms: 1.02x slower                                                    |
| docutils                 | 2.92 sec                                                               | 2.97 sec: 1.02x slower                                                   |
| gunicorn                 | 1.29 ms                                                                | 1.31 ms: 1.02x slower                                                    |
| raytrace                 | 270 ms                                                                 | 276 ms: 1.02x slower                                                     |
| fannkuch                 | 395 ms                                                                 | 403 ms: 1.02x slower                                                     |
| typing_runtime_protocols | 113 us                                                                 | 116 us: 1.02x slower                                                     |
| sympy_sum                | 167 ms                                                                 | 171 ms: 1.03x slower                                                     |
| sympy_integrate          | 22.1 ms                                                                | 22.6 ms: 1.03x slower                                                    |
| nqueens                  | 90.7 ms                                                                | 93.1 ms: 1.03x slower                                                    |
| pylint                   | 296 ms                                                                 | 304 ms: 1.03x slower                                                     |
| hexiom                   | 6.96 ms                                                                | 7.17 ms: 1.03x slower                                                    |
| unpickle_list            | 5.17 us                                                                | 5.32 us: 1.03x slower                                                    |
| genshi_text              | 23.9 ms                                                                | 24.7 ms: 1.03x slower                                                    |
| asyncio_tcp              | 511 ms                                                                 | 527 ms: 1.03x slower                                                     |
| coroutines               | 21.9 ms                                                                | 22.5 ms: 1.03x slower                                                    |
| scimark_sor              | 133 ms                                                                 | 138 ms: 1.04x slower                                                     |
| mypy2                    | 781 ms                                                                 | 812 ms: 1.04x slower                                                     |
| comprehensions           | 17.8 us                                                                | 18.6 us: 1.04x slower                                                    |
| deltablue                | 3.65 ms                                                                | 3.82 ms: 1.05x slower                                                    |
| genshi_xml               | 52.6 ms                                                                | 55.4 ms: 1.05x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (31): unpickle, async_tree_memoization, bench_mp_pool, scimark_sparse_mat_mult, scimark_lu, thrift, nbody, asyncio_websockets, sqlglot_parse, pprint_safe_repr, dulwich_log, richards, logging_format, xml_etree_process, float, deepcopy_memo, async_tree_io, sqlite_synth, telco, pprint_pformat, async_tree_io_tg, unpickle_pure_python, json, pycparser, dask, async_tree_none_tg, xml_etree_parse, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
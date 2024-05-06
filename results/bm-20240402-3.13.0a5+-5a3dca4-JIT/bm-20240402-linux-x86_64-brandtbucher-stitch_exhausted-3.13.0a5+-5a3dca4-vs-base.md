# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.01x slower
- HPT reliability: 99.71%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 278 ms                                                                 | 282 ms: 1.01x slower                                                     |
| chameleon      | 6.95 ms                                                                | 7.06 ms: 1.02x slower                                                    |
| docutils       | 2.89 sec                                                               | 2.94 sec: 1.02x slower                                                   |
| tornado_http   | 96.9 ms                                                                | 96.5 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.6 ms                                                                | 24.7 ms: 1.00x slower                                                    |
| regex_dna      | 220 ms                                                                 | 221 ms: 1.00x slower                                                     |
| regex_effbot   | 3.67 ms                                                                | 3.75 ms: 1.02x slower                                                    |
| regex_compile  | 146 ms                                                                 | 149 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|---------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_generate  | 88.9 ms                                                                | 86.7 ms: 1.03x faster                                                    |
| xml_etree_process   | 61.1 ms                                                                | 59.8 ms: 1.02x faster                                                    |
| tomli_loads         | 2.09 sec                                                               | 2.06 sec: 1.02x faster                                                   |
| unpickle_list       | 5.24 us                                                                | 5.19 us: 1.01x faster                                                    |
| pickle_list         | 5.00 us                                                                | 4.96 us: 1.01x faster                                                    |
| xml_etree_iterparse | 107 ms                                                                 | 107 ms: 1.00x faster                                                     |
| json_loads          | 28.7 us                                                                | 29.0 us: 1.01x slower                                                    |
| json_dumps          | 10.4 ms                                                                | 10.7 ms: 1.03x slower                                                    |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (6): xml_etree_parse, pickle, pickle_dict, pickle_pure_python, unpickle_pure_python, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                                    |
| python_startup_no_site | 9.49 ms                                                                | 9.51 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 25.7 ms                                                                | 24.8 ms: 1.04x faster                                                    |
| genshi_xml      | 56.4 ms                                                                | 55.7 ms: 1.01x faster                                                    |
| mako            | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                                    |
| django_template | 35.7 ms                                                                | 37.1 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text              | 25.7 ms                                                                | 24.8 ms: 1.04x faster                                                    |
| scimark_lu               | 134 ms                                                                 | 130 ms: 1.03x faster                                                     |
| xml_etree_generate       | 88.9 ms                                                                | 86.7 ms: 1.03x faster                                                    |
| spectral_norm            | 117 ms                                                                 | 114 ms: 1.02x faster                                                     |
| scimark_fft              | 351 ms                                                                 | 343 ms: 1.02x faster                                                     |
| coverage                 | 98.0 ms                                                                | 95.8 ms: 1.02x faster                                                    |
| xml_etree_process        | 61.1 ms                                                                | 59.8 ms: 1.02x faster                                                    |
| unpack_sequence          | 87.2 ns                                                                | 85.6 ns: 1.02x faster                                                    |
| pycparser                | 1.21 sec                                                               | 1.18 sec: 1.02x faster                                                   |
| scimark_sparse_mat_mult  | 4.95 ms                                                                | 4.87 ms: 1.02x faster                                                    |
| sqlglot_parse            | 1.34 ms                                                                | 1.32 ms: 1.02x faster                                                    |
| logging_format           | 6.52 us                                                                | 6.42 us: 1.02x faster                                                    |
| tomli_loads              | 2.09 sec                                                               | 2.06 sec: 1.02x faster                                                   |
| richards                 | 47.0 ms                                                                | 46.4 ms: 1.01x faster                                                    |
| genshi_xml               | 56.4 ms                                                                | 55.7 ms: 1.01x faster                                                    |
| fannkuch                 | 394 ms                                                                 | 390 ms: 1.01x faster                                                     |
| sqlglot_transpile        | 1.65 ms                                                                | 1.64 ms: 1.01x faster                                                    |
| async_generators         | 463 ms                                                                 | 458 ms: 1.01x faster                                                     |
| unpickle_list            | 5.24 us                                                                | 5.19 us: 1.01x faster                                                    |
| logging_simple           | 5.90 us                                                                | 5.84 us: 1.01x faster                                                    |
| pickle_list              | 5.00 us                                                                | 4.96 us: 1.01x faster                                                    |
| sqlite_synth             | 2.88 us                                                                | 2.86 us: 1.01x faster                                                    |
| asyncio_websockets       | 570 ms                                                                 | 567 ms: 1.01x faster                                                     |
| sqlglot_optimize         | 58.3 ms                                                                | 58.0 ms: 1.00x faster                                                    |
| tornado_http             | 96.9 ms                                                                | 96.5 ms: 1.00x faster                                                    |
| xml_etree_iterparse      | 107 ms                                                                 | 107 ms: 1.00x faster                                                     |
| create_gc_cycles         | 1.69 ms                                                                | 1.68 ms: 1.00x faster                                                    |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                                    |
| python_startup_no_site   | 9.49 ms                                                                | 9.51 ms: 1.00x slower                                                    |
| regex_v8                 | 24.6 ms                                                                | 24.7 ms: 1.00x slower                                                    |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                   |
| regex_dna                | 220 ms                                                                 | 221 ms: 1.00x slower                                                     |
| meteor_contest           | 111 ms                                                                 | 111 ms: 1.01x slower                                                     |
| sqlglot_normalize        | 113 ms                                                                 | 114 ms: 1.01x slower                                                     |
| generators               | 29.9 ms                                                                | 30.1 ms: 1.01x slower                                                    |
| typing_runtime_protocols | 113 us                                                                 | 114 us: 1.01x slower                                                     |
| aiohttp                  | 1.21 ms                                                                | 1.22 ms: 1.01x slower                                                    |
| coroutines               | 22.6 ms                                                                | 22.8 ms: 1.01x slower                                                    |
| bench_thread_pool        | 851 us                                                                 | 859 us: 1.01x slower                                                     |
| json_loads               | 28.7 us                                                                | 29.0 us: 1.01x slower                                                    |
| 2to3                     | 278 ms                                                                 | 282 ms: 1.01x slower                                                     |
| dulwich_log              | 70.6 ms                                                                | 71.4 ms: 1.01x slower                                                    |
| deepcopy_memo            | 38.8 us                                                                | 39.3 us: 1.01x slower                                                    |
| hexiom                   | 7.24 ms                                                                | 7.33 ms: 1.01x slower                                                    |
| crypto_pyaes             | 74.4 ms                                                                | 75.3 ms: 1.01x slower                                                    |
| comprehensions           | 18.3 us                                                                | 18.5 us: 1.01x slower                                                    |
| pprint_pformat           | 1.53 sec                                                               | 1.55 sec: 1.02x slower                                                   |
| chameleon                | 6.95 ms                                                                | 7.06 ms: 1.02x slower                                                    |
| raytrace                 | 291 ms                                                                 | 296 ms: 1.02x slower                                                     |
| chaos                    | 63.0 ms                                                                | 64.1 ms: 1.02x slower                                                    |
| docutils                 | 2.89 sec                                                               | 2.94 sec: 1.02x slower                                                   |
| sympy_str                | 289 ms                                                                 | 294 ms: 1.02x slower                                                     |
| go                       | 155 ms                                                                 | 158 ms: 1.02x slower                                                     |
| nqueens                  | 91.6 ms                                                                | 93.5 ms: 1.02x slower                                                    |
| sympy_sum                | 164 ms                                                                 | 167 ms: 1.02x slower                                                     |
| pyflate                  | 481 ms                                                                 | 491 ms: 1.02x slower                                                     |
| regex_effbot             | 3.67 ms                                                                | 3.75 ms: 1.02x slower                                                    |
| regex_compile            | 146 ms                                                                 | 149 ms: 1.02x slower                                                     |
| pylint                   | 299 ms                                                                 | 306 ms: 1.02x slower                                                     |
| asyncio_tcp              | 505 ms                                                                 | 518 ms: 1.03x slower                                                     |
| json_dumps               | 10.4 ms                                                                | 10.7 ms: 1.03x slower                                                    |
| sympy_expand             | 488 ms                                                                 | 501 ms: 1.03x slower                                                     |
| mypy2                    | 788 ms                                                                 | 812 ms: 1.03x slower                                                     |
| sympy_integrate          | 21.6 ms                                                                | 22.3 ms: 1.03x slower                                                    |
| mako                     | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                                    |
| pprint_safe_repr         | 739 ms                                                                 | 766 ms: 1.04x slower                                                     |
| django_template          | 35.7 ms                                                                | 37.1 ms: 1.04x slower                                                    |
| json                     | 5.33 ms                                                                | 5.54 ms: 1.04x slower                                                    |
| djangocms                | 31.2 us                                                                | 32.5 us: 1.04x slower                                                    |
| gc_traversal             | 3.78 ms                                                                | 3.99 ms: 1.06x slower                                                    |
| mdp                      | 2.65 sec                                                               | 2.82 sec: 1.06x slower                                                   |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (31): xml_etree_parse, async_tree_none, deepcopy_reduce, deepcopy, pickle, richards_super, async_tree_memoization_tg, logging_silent, bench_mp_pool, async_tree_io_tg, pickle_dict, async_tree_none_tg, pickle_pure_python, unpickle_pure_python, pidigits, deltablue, scimark_sor, async_tree_memoization, nbody, thrift, scimark_monte_carlo, float, pathlib, dask, async_tree_cpu_io_mixed_tg, html5lib, gunicorn, async_tree_cpu_io_mixed, telco, async_tree_io, unpickle

# HPT report

- Reliability score: 99.71% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x
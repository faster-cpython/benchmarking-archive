# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.01x faster
- HPT reliability: 98.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                       | 300 ms: 1.00x slower                                                       |
| chameleon      | 7.42 ms                                                                      | 7.36 ms: 1.01x faster                                                      |
| docutils       | 3.08 sec                                                                     | 3.07 sec: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                               |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 78.4 ms                                                                      | 75.4 ms: 1.04x faster                                                      |
| nbody          | 95.9 ms                                                                      | 93.1 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                                        | 1.02x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.69 ms                                                                      | 3.54 ms: 1.04x faster                                                      |
| regex_compile  | 147 ms                                                                       | 146 ms: 1.01x faster                                                       |
| regex_v8       | 25.6 ms                                                                      | 25.4 ms: 1.01x faster                                                      |
| regex_dna      | 236 ms                                                                       | 239 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_parse      | 154 ms                                                                       | 144 ms: 1.07x faster                                                       |
| pickle_list          | 4.46 us                                                                      | 4.28 us: 1.04x faster                                                      |
| tomli_loads          | 2.17 sec                                                                     | 2.10 sec: 1.03x faster                                                     |
| xml_etree_iterparse  | 106 ms                                                                       | 103 ms: 1.02x faster                                                       |
| unpickle_list        | 4.75 us                                                                      | 4.64 us: 1.02x faster                                                      |
| unpickle_pure_python | 234 us                                                                       | 229 us: 1.02x faster                                                       |
| pickle_pure_python   | 318 us                                                                       | 312 us: 1.02x faster                                                       |
| xml_etree_generate   | 84.1 ms                                                                      | 83.3 ms: 1.01x faster                                                      |
| json_loads           | 25.4 us                                                                      | 25.5 us: 1.01x slower                                                      |
| pickle               | 10.5 us                                                                      | 10.6 us: 1.01x slower                                                      |
| json_dumps           | 10.6 ms                                                                      | 10.8 ms: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (3): pickle_dict, xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                                      | 9.29 ms: 1.08x faster                                                      |
| genshi_xml      | 58.4 ms                                                                      | 57.2 ms: 1.02x faster                                                      |
| django_template | 39.6 ms                                                                      | 40.4 ms: 1.02x slower                                                      |
| Geometric mean  | (ref)                                                                        | 1.02x faster                                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| spectral_norm            | 93.2 ms                                                                      | 81.9 ms: 1.14x faster                                                      |
| scimark_lu               | 126 ms                                                                       | 115 ms: 1.09x faster                                                       |
| scimark_monte_carlo      | 73.1 ms                                                                      | 66.9 ms: 1.09x faster                                                      |
| chaos                    | 68.4 ms                                                                      | 62.8 ms: 1.09x faster                                                      |
| pyflate                  | 492 ms                                                                       | 454 ms: 1.09x faster                                                       |
| scimark_fft              | 315 ms                                                                       | 290 ms: 1.09x faster                                                       |
| mako                     | 10.0 ms                                                                      | 9.29 ms: 1.08x faster                                                      |
| fannkuch                 | 374 ms                                                                       | 349 ms: 1.07x faster                                                       |
| crypto_pyaes             | 77.3 ms                                                                      | 72.5 ms: 1.07x faster                                                      |
| xml_etree_parse          | 154 ms                                                                       | 144 ms: 1.07x faster                                                       |
| hexiom                   | 7.49 ms                                                                      | 7.09 ms: 1.06x faster                                                      |
| generators               | 34.6 ms                                                                      | 33.1 ms: 1.05x faster                                                      |
| pickle_list              | 4.46 us                                                                      | 4.28 us: 1.04x faster                                                      |
| regex_effbot             | 3.69 ms                                                                      | 3.54 ms: 1.04x faster                                                      |
| comprehensions           | 19.7 us                                                                      | 19.0 us: 1.04x faster                                                      |
| float                    | 78.4 ms                                                                      | 75.4 ms: 1.04x faster                                                      |
| richards_super           | 58.9 ms                                                                      | 56.7 ms: 1.04x faster                                                      |
| scimark_sor              | 154 ms                                                                       | 148 ms: 1.04x faster                                                       |
| pprint_safe_repr         | 839 ms                                                                       | 811 ms: 1.03x faster                                                       |
| pprint_pformat           | 1.70 sec                                                                     | 1.65 sec: 1.03x faster                                                     |
| tomli_loads              | 2.17 sec                                                                     | 2.10 sec: 1.03x faster                                                     |
| nbody                    | 95.9 ms                                                                      | 93.1 ms: 1.03x faster                                                      |
| sqlglot_parse            | 1.44 ms                                                                      | 1.40 ms: 1.03x faster                                                      |
| coverage                 | 81.7 ms                                                                      | 79.7 ms: 1.02x faster                                                      |
| richards                 | 51.7 ms                                                                      | 50.5 ms: 1.02x faster                                                      |
| xml_etree_iterparse      | 106 ms                                                                       | 103 ms: 1.02x faster                                                       |
| unpickle_list            | 4.75 us                                                                      | 4.64 us: 1.02x faster                                                      |
| telco                    | 8.21 ms                                                                      | 8.04 ms: 1.02x faster                                                      |
| genshi_xml               | 58.4 ms                                                                      | 57.2 ms: 1.02x faster                                                      |
| unpickle_pure_python     | 234 us                                                                       | 229 us: 1.02x faster                                                       |
| pickle_pure_python       | 318 us                                                                       | 312 us: 1.02x faster                                                       |
| sqlglot_transpile        | 1.84 ms                                                                      | 1.81 ms: 1.02x faster                                                      |
| nqueens                  | 104 ms                                                                       | 102 ms: 1.02x faster                                                       |
| mdp                      | 2.64 sec                                                                     | 2.60 sec: 1.01x faster                                                     |
| xml_etree_generate       | 84.1 ms                                                                      | 83.3 ms: 1.01x faster                                                      |
| chameleon                | 7.42 ms                                                                      | 7.36 ms: 1.01x faster                                                      |
| regex_compile            | 147 ms                                                                       | 146 ms: 1.01x faster                                                       |
| regex_v8                 | 25.6 ms                                                                      | 25.4 ms: 1.01x faster                                                      |
| dulwich_log              | 69.3 ms                                                                      | 68.9 ms: 1.01x faster                                                      |
| docutils                 | 3.08 sec                                                                     | 3.07 sec: 1.00x faster                                                     |
| pylint                   | 337 ms                                                                       | 337 ms: 1.00x faster                                                       |
| asyncio_tcp_ssl          | 1.58 sec                                                                     | 1.58 sec: 1.00x slower                                                     |
| 2to3                     | 299 ms                                                                       | 300 ms: 1.00x slower                                                       |
| json_loads               | 25.4 us                                                                      | 25.5 us: 1.01x slower                                                      |
| sympy_sum                | 160 ms                                                                       | 161 ms: 1.01x slower                                                       |
| create_gc_cycles         | 1.81 ms                                                                      | 1.82 ms: 1.01x slower                                                      |
| coroutines               | 22.4 ms                                                                      | 22.6 ms: 1.01x slower                                                      |
| deepcopy_reduce          | 3.32 us                                                                      | 3.34 us: 1.01x slower                                                      |
| sympy_str                | 300 ms                                                                       | 303 ms: 1.01x slower                                                       |
| sympy_integrate          | 25.0 ms                                                                      | 25.2 ms: 1.01x slower                                                      |
| pickle                   | 10.5 us                                                                      | 10.6 us: 1.01x slower                                                      |
| scimark_sparse_mat_mult  | 4.15 ms                                                                      | 4.19 ms: 1.01x slower                                                      |
| go                       | 173 ms                                                                       | 175 ms: 1.01x slower                                                       |
| logging_simple           | 6.65 us                                                                      | 6.72 us: 1.01x slower                                                      |
| asyncio_tcp              | 371 ms                                                                       | 375 ms: 1.01x slower                                                       |
| typing_runtime_protocols | 119 us                                                                       | 120 us: 1.01x slower                                                       |
| logging_silent           | 97.5 ns                                                                      | 98.6 ns: 1.01x slower                                                      |
| pathlib                  | 19.4 ms                                                                      | 19.7 ms: 1.01x slower                                                      |
| pycparser                | 1.25 sec                                                                     | 1.26 sec: 1.01x slower                                                     |
| regex_dna                | 236 ms                                                                       | 239 ms: 1.01x slower                                                       |
| json                     | 5.41 ms                                                                      | 5.48 ms: 1.01x slower                                                      |
| deepcopy_memo            | 38.0 us                                                                      | 38.5 us: 1.01x slower                                                      |
| asyncio_websockets       | 387 ms                                                                       | 393 ms: 1.02x slower                                                       |
| json_dumps               | 10.6 ms                                                                      | 10.8 ms: 1.02x slower                                                      |
| logging_format           | 7.25 us                                                                      | 7.38 us: 1.02x slower                                                      |
| sympy_expand             | 503 ms                                                                       | 513 ms: 1.02x slower                                                       |
| thrift                   | 878 us                                                                       | 897 us: 1.02x slower                                                       |
| django_template          | 39.6 ms                                                                      | 40.4 ms: 1.02x slower                                                      |
| deepcopy                 | 378 us                                                                       | 389 us: 1.03x slower                                                       |
| async_generators         | 383 ms                                                                       | 395 ms: 1.03x slower                                                       |
| unpack_sequence          | 59.6 ns                                                                      | 89.5 ns: 1.50x slower                                                      |
| Geometric mean           | (ref)                                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (30): html5lib, async_tree_io, genshi_text, async_tree_cpu_io_mixed, async_tree_memoization, aiohttp, bench_mp_pool, async_tree_memoization_tg, meteor_contest, sqlite_synth, pickle_dict, pidigits, python_startup_no_site, sqlglot_normalize, gc_traversal, async_tree_none, deltablue, python_startup, async_tree_cpu_io_mixed_tg, tornado_http, sqlglot_optimize, async_tree_io_tg, dask, bench_thread_pool, xml_etree_process, unpickle, gunicorn, raytrace, async_tree_none_tg, mypy2

# HPT report

- Reliability score: 98.89% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
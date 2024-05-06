# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.02x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 301 ms                                                                       | 303 ms: 1.01x slower                                                       |
| chameleon      | 7.67 ms                                                                      | 7.52 ms: 1.02x faster                                                      |
| docutils       | 3.09 sec                                                                     | 3.11 sec: 1.01x slower                                                     |
| html5lib       | 73.6 ms                                                                      | 74.2 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none  | 379 ms                                                                       | 362 ms: 1.05x faster                                                       |
| async_tree_io_tg | 884 ms                                                                       | 912 ms: 1.03x slower                                                       |
| Geometric mean   | (ref)                                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 261 ms                                                                       | 262 ms: 1.00x slower                                                       |
| float          | 77.9 ms                                                                      | 78.6 ms: 1.01x slower                                                      |
| nbody          | 97.7 ms                                                                      | 103 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                                        | 1.02x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 243 ms                                                                       | 245 ms: 1.01x slower                                                       |
| regex_effbot   | 3.64 ms                                                                      | 3.69 ms: 1.01x slower                                                      |
| regex_v8       | 25.4 ms                                                                      | 25.8 ms: 1.01x slower                                                      |
| regex_compile  | 148 ms                                                                       | 151 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle             | 15.5 us                                                                      | 14.8 us: 1.05x faster                                                      |
| unpickle_list        | 4.73 us                                                                      | 4.56 us: 1.04x faster                                                      |
| xml_etree_parse      | 147 ms                                                                       | 144 ms: 1.02x faster                                                       |
| pickle               | 10.5 us                                                                      | 10.4 us: 1.01x faster                                                      |
| xml_etree_process    | 58.5 ms                                                                      | 58.9 ms: 1.01x slower                                                      |
| xml_etree_generate   | 84.1 ms                                                                      | 86.0 ms: 1.02x slower                                                      |
| json_loads           | 24.9 us                                                                      | 25.6 us: 1.02x slower                                                      |
| pickle_list          | 4.34 us                                                                      | 4.49 us: 1.03x slower                                                      |
| unpickle_pure_python | 234 us                                                                       | 244 us: 1.04x slower                                                       |
| tomli_loads          | 2.18 sec                                                                     | 2.36 sec: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                                        | 1.01x slower                                                               |

Benchmark hidden because not significant (4): pickle_dict, json_dumps, pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                      |
| python_startup         | 13.5 ms                                                                      | 13.5 ms: 1.00x slower                                                      |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 60.1 ms                                                                      | 58.6 ms: 1.03x faster                                                      |
| genshi_text     | 27.2 ms                                                                      | 26.6 ms: 1.02x faster                                                      |
| django_template | 40.0 ms                                                                      | 39.7 ms: 1.01x faster                                                      |
| mako            | 9.96 ms                                                                      | 10.2 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                                        | 1.01x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| gc_traversal             | 4.60 ms                                                                      | 4.36 ms: 1.06x faster                                                      |
| unpickle                 | 15.5 us                                                                      | 14.8 us: 1.05x faster                                                      |
| async_tree_none          | 379 ms                                                                       | 362 ms: 1.05x faster                                                       |
| unpickle_list            | 4.73 us                                                                      | 4.56 us: 1.04x faster                                                      |
| deepcopy_reduce          | 3.48 us                                                                      | 3.37 us: 1.03x faster                                                      |
| pathlib                  | 19.8 ms                                                                      | 19.2 ms: 1.03x faster                                                      |
| genshi_xml               | 60.1 ms                                                                      | 58.6 ms: 1.03x faster                                                      |
| generators               | 33.9 ms                                                                      | 33.1 ms: 1.02x faster                                                      |
| sqlglot_normalize        | 124 ms                                                                       | 121 ms: 1.02x faster                                                       |
| genshi_text              | 27.2 ms                                                                      | 26.6 ms: 1.02x faster                                                      |
| chameleon                | 7.67 ms                                                                      | 7.52 ms: 1.02x faster                                                      |
| thrift                   | 877 us                                                                       | 861 us: 1.02x faster                                                       |
| typing_runtime_protocols | 121 us                                                                       | 119 us: 1.02x faster                                                       |
| xml_etree_parse          | 147 ms                                                                       | 144 ms: 1.02x faster                                                       |
| coverage                 | 81.7 ms                                                                      | 80.3 ms: 1.02x faster                                                      |
| deepcopy_memo            | 39.2 us                                                                      | 38.5 us: 1.02x faster                                                      |
| logging_simple           | 6.81 us                                                                      | 6.73 us: 1.01x faster                                                      |
| pickle                   | 10.5 us                                                                      | 10.4 us: 1.01x faster                                                      |
| deepcopy                 | 398 us                                                                       | 395 us: 1.01x faster                                                       |
| django_template          | 40.0 ms                                                                      | 39.7 ms: 1.01x faster                                                      |
| sqlglot_optimize         | 63.4 ms                                                                      | 62.9 ms: 1.01x faster                                                      |
| sympy_expand             | 508 ms                                                                       | 505 ms: 1.00x faster                                                       |
| dulwich_log              | 69.8 ms                                                                      | 69.4 ms: 1.00x faster                                                      |
| python_startup_no_site   | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                      |
| python_startup           | 13.5 ms                                                                      | 13.5 ms: 1.00x slower                                                      |
| mdp                      | 2.65 sec                                                                     | 2.65 sec: 1.00x slower                                                     |
| sympy_str                | 301 ms                                                                       | 302 ms: 1.00x slower                                                       |
| pidigits                 | 261 ms                                                                       | 262 ms: 1.00x slower                                                       |
| asyncio_tcp              | 370 ms                                                                       | 372 ms: 1.01x slower                                                       |
| docutils                 | 3.09 sec                                                                     | 3.11 sec: 1.01x slower                                                     |
| pylint                   | 338 ms                                                                       | 340 ms: 1.01x slower                                                       |
| json                     | 5.37 ms                                                                      | 5.40 ms: 1.01x slower                                                      |
| xml_etree_process        | 58.5 ms                                                                      | 58.9 ms: 1.01x slower                                                      |
| sqlglot_transpile        | 1.81 ms                                                                      | 1.83 ms: 1.01x slower                                                      |
| 2to3                     | 301 ms                                                                       | 303 ms: 1.01x slower                                                       |
| sympy_sum                | 161 ms                                                                       | 162 ms: 1.01x slower                                                       |
| sympy_integrate          | 25.2 ms                                                                      | 25.4 ms: 1.01x slower                                                      |
| create_gc_cycles         | 1.78 ms                                                                      | 1.80 ms: 1.01x slower                                                      |
| regex_dna                | 243 ms                                                                       | 245 ms: 1.01x slower                                                       |
| html5lib                 | 73.6 ms                                                                      | 74.2 ms: 1.01x slower                                                      |
| coroutines               | 22.3 ms                                                                      | 22.5 ms: 1.01x slower                                                      |
| float                    | 77.9 ms                                                                      | 78.6 ms: 1.01x slower                                                      |
| deltablue                | 3.76 ms                                                                      | 3.80 ms: 1.01x slower                                                      |
| raytrace                 | 302 ms                                                                       | 306 ms: 1.01x slower                                                       |
| regex_effbot             | 3.64 ms                                                                      | 3.69 ms: 1.01x slower                                                      |
| regex_v8                 | 25.4 ms                                                                      | 25.8 ms: 1.01x slower                                                      |
| logging_silent           | 97.5 ns                                                                      | 99.0 ns: 1.01x slower                                                      |
| asyncio_websockets       | 386 ms                                                                       | 392 ms: 1.02x slower                                                       |
| meteor_contest           | 132 ms                                                                       | 134 ms: 1.02x slower                                                       |
| sqlite_synth             | 2.69 us                                                                      | 2.74 us: 1.02x slower                                                      |
| regex_compile            | 148 ms                                                                       | 151 ms: 1.02x slower                                                       |
| xml_etree_generate       | 84.1 ms                                                                      | 86.0 ms: 1.02x slower                                                      |
| comprehensions           | 19.9 us                                                                      | 20.4 us: 1.02x slower                                                      |
| json_loads               | 24.9 us                                                                      | 25.6 us: 1.02x slower                                                      |
| richards_super           | 58.6 ms                                                                      | 60.2 ms: 1.03x slower                                                      |
| mako                     | 9.96 ms                                                                      | 10.2 ms: 1.03x slower                                                      |
| async_tree_io_tg         | 884 ms                                                                       | 912 ms: 1.03x slower                                                       |
| pickle_list              | 4.34 us                                                                      | 4.49 us: 1.03x slower                                                      |
| richards                 | 51.6 ms                                                                      | 53.7 ms: 1.04x slower                                                      |
| scimark_sor              | 154 ms                                                                       | 160 ms: 1.04x slower                                                       |
| unpickle_pure_python     | 234 us                                                                       | 244 us: 1.04x slower                                                       |
| pprint_pformat           | 1.72 sec                                                                     | 1.79 sec: 1.04x slower                                                     |
| go                       | 174 ms                                                                       | 182 ms: 1.04x slower                                                       |
| crypto_pyaes             | 77.6 ms                                                                      | 81.1 ms: 1.05x slower                                                      |
| pyflate                  | 499 ms                                                                       | 522 ms: 1.05x slower                                                       |
| chaos                    | 66.4 ms                                                                      | 69.8 ms: 1.05x slower                                                      |
| spectral_norm            | 94.2 ms                                                                      | 99.0 ms: 1.05x slower                                                      |
| scimark_lu               | 123 ms                                                                       | 130 ms: 1.05x slower                                                       |
| nbody                    | 97.7 ms                                                                      | 103 ms: 1.05x slower                                                       |
| nqueens                  | 103 ms                                                                       | 109 ms: 1.06x slower                                                       |
| hexiom                   | 7.54 ms                                                                      | 8.00 ms: 1.06x slower                                                      |
| scimark_monte_carlo      | 73.3 ms                                                                      | 77.9 ms: 1.06x slower                                                      |
| scimark_fft              | 316 ms                                                                       | 341 ms: 1.08x slower                                                       |
| scimark_sparse_mat_mult  | 4.17 ms                                                                      | 4.50 ms: 1.08x slower                                                      |
| pprint_safe_repr         | 833 ms                                                                       | 902 ms: 1.08x slower                                                       |
| tomli_loads              | 2.18 sec                                                                     | 2.36 sec: 1.09x slower                                                     |
| fannkuch                 | 374 ms                                                                       | 408 ms: 1.09x slower                                                       |
| unpack_sequence          | 59.5 ns                                                                      | 107 ns: 1.79x slower                                                       |
| Geometric mean           | (ref)                                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (23): async_tree_memoization, bench_mp_pool, async_tree_cpu_io_mixed_tg, async_tree_io, pickle_dict, telco, async_tree_none_tg, logging_format, json_dumps, dask, pycparser, asyncio_tcp_ssl, async_tree_cpu_io_mixed, tornado_http, async_generators, pickle_pure_python, sqlglot_parse, bench_thread_pool, gunicorn, aiohttp, mypy2, xml_etree_iterparse, async_tree_memoization_tg

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x
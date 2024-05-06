# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 9759712
- commit date: 2024-04-17
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 276 ms: 1.01x faster                                                       |
| chameleon      | 6.94 ms                                                                | 7.12 ms: 1.03x slower                                                      |
| html5lib       | 67.2 ms                                                                | 67.9 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 90.9 ms                                                                | 77.1 ms: 1.18x faster                                                      |
| pidigits       | 211 ms                                                                 | 189 ms: 1.12x faster                                                       |
| float          | 77.0 ms                                                                | 72.9 ms: 1.06x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 143 ms                                                                 | 140 ms: 1.02x faster                                                       |
| regex_dna      | 227 ms                                                                 | 225 ms: 1.01x faster                                                       |
| regex_v8       | 25.9 ms                                                                | 25.8 ms: 1.00x faster                                                      |
| regex_effbot   | 3.67 ms                                                                | 3.77 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle             | 16.8 us                                                                | 15.3 us: 1.10x faster                                                      |
| unpickle_pure_python | 236 us                                                                 | 224 us: 1.05x faster                                                       |
| tomli_loads          | 2.02 sec                                                               | 1.93 sec: 1.05x faster                                                     |
| unpickle_list        | 5.33 us                                                                | 5.12 us: 1.04x faster                                                      |
| pickle               | 12.0 us                                                                | 11.6 us: 1.04x faster                                                      |
| pickle_list          | 5.06 us                                                                | 4.91 us: 1.03x faster                                                      |
| xml_etree_iterparse  | 109 ms                                                                 | 106 ms: 1.03x faster                                                       |
| xml_etree_process    | 60.5 ms                                                                | 59.5 ms: 1.02x faster                                                      |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.02x faster                                                      |
| xml_etree_generate   | 87.8 ms                                                                | 87.2 ms: 1.01x faster                                                      |
| json_loads           | 27.7 us                                                                | 27.8 us: 1.00x slower                                                      |
| pickle_dict          | 33.9 us                                                                | 34.1 us: 1.00x slower                                                      |
| xml_etree_parse      | 159 ms                                                                 | 161 ms: 1.01x slower                                                       |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| python_startup_no_site | 7.59 ms                                                                | 7.66 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.1 ms: 1.06x faster                                                      |
| django_template | 36.5 ms                                                                | 35.6 ms: 1.02x faster                                                      |
| genshi_text     | 24.2 ms                                                                | 23.9 ms: 1.01x faster                                                      |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody                   | 90.9 ms                                                                | 77.1 ms: 1.18x faster                                                      |
| spectral_norm           | 114 ms                                                                 | 99.8 ms: 1.14x faster                                                      |
| fannkuch                | 399 ms                                                                 | 350 ms: 1.14x faster                                                       |
| scimark_fft             | 342 ms                                                                 | 304 ms: 1.12x faster                                                       |
| pidigits                | 211 ms                                                                 | 189 ms: 1.12x faster                                                       |
| scimark_sparse_mat_mult | 4.83 ms                                                                | 4.34 ms: 1.11x faster                                                      |
| scimark_monte_carlo     | 70.2 ms                                                                | 63.4 ms: 1.11x faster                                                      |
| unpickle                | 16.8 us                                                                | 15.3 us: 1.10x faster                                                      |
| crypto_pyaes            | 74.4 ms                                                                | 68.5 ms: 1.09x faster                                                      |
| pyflate                 | 474 ms                                                                 | 441 ms: 1.07x faster                                                       |
| pprint_pformat          | 1.58 sec                                                               | 1.48 sec: 1.07x faster                                                     |
| mako                    | 10.7 ms                                                                | 10.1 ms: 1.06x faster                                                      |
| float                   | 77.0 ms                                                                | 72.9 ms: 1.06x faster                                                      |
| scimark_lu              | 131 ms                                                                 | 124 ms: 1.05x faster                                                       |
| unpickle_pure_python    | 236 us                                                                 | 224 us: 1.05x faster                                                       |
| scimark_sor             | 132 ms                                                                 | 126 ms: 1.05x faster                                                       |
| comprehensions          | 18.0 us                                                                | 17.2 us: 1.05x faster                                                      |
| tomli_loads             | 2.02 sec                                                               | 1.93 sec: 1.05x faster                                                     |
| chaos                   | 62.9 ms                                                                | 60.2 ms: 1.04x faster                                                      |
| go                      | 153 ms                                                                 | 147 ms: 1.04x faster                                                       |
| unpickle_list           | 5.33 us                                                                | 5.12 us: 1.04x faster                                                      |
| hexiom                  | 6.99 ms                                                                | 6.71 ms: 1.04x faster                                                      |
| pickle                  | 12.0 us                                                                | 11.6 us: 1.04x faster                                                      |
| pickle_list             | 5.06 us                                                                | 4.91 us: 1.03x faster                                                      |
| pprint_safe_repr        | 743 ms                                                                 | 722 ms: 1.03x faster                                                       |
| xml_etree_iterparse     | 109 ms                                                                 | 106 ms: 1.03x faster                                                       |
| django_template         | 36.5 ms                                                                | 35.6 ms: 1.02x faster                                                      |
| telco                   | 8.72 ms                                                                | 8.52 ms: 1.02x faster                                                      |
| regex_compile           | 143 ms                                                                 | 140 ms: 1.02x faster                                                       |
| mdp                     | 2.81 sec                                                               | 2.75 sec: 1.02x faster                                                     |
| xml_etree_process       | 60.5 ms                                                                | 59.5 ms: 1.02x faster                                                      |
| json_dumps              | 10.6 ms                                                                | 10.5 ms: 1.02x faster                                                      |
| generators              | 30.1 ms                                                                | 29.6 ms: 1.02x faster                                                      |
| richards_super          | 49.2 ms                                                                | 48.5 ms: 1.01x faster                                                      |
| meteor_contest          | 110 ms                                                                 | 109 ms: 1.01x faster                                                       |
| genshi_text             | 24.2 ms                                                                | 23.9 ms: 1.01x faster                                                      |
| sqlglot_optimize        | 58.1 ms                                                                | 57.3 ms: 1.01x faster                                                      |
| nqueens                 | 89.3 ms                                                                | 88.2 ms: 1.01x faster                                                      |
| sqlite_synth            | 2.90 us                                                                | 2.87 us: 1.01x faster                                                      |
| regex_dna               | 227 ms                                                                 | 225 ms: 1.01x faster                                                       |
| create_gc_cycles        | 1.77 ms                                                                | 1.75 ms: 1.01x faster                                                      |
| logging_simple          | 5.80 us                                                                | 5.74 us: 1.01x faster                                                      |
| sqlglot_transpile       | 1.64 ms                                                                | 1.63 ms: 1.01x faster                                                      |
| raytrace                | 272 ms                                                                 | 270 ms: 1.01x faster                                                       |
| coverage                | 98.7 ms                                                                | 97.8 ms: 1.01x faster                                                      |
| sqlglot_normalize       | 114 ms                                                                 | 113 ms: 1.01x faster                                                       |
| json                    | 5.12 ms                                                                | 5.08 ms: 1.01x faster                                                      |
| sympy_str               | 297 ms                                                                 | 295 ms: 1.01x faster                                                       |
| xml_etree_generate      | 87.8 ms                                                                | 87.2 ms: 1.01x faster                                                      |
| sqlglot_parse           | 1.32 ms                                                                | 1.31 ms: 1.01x faster                                                      |
| 2to3                    | 277 ms                                                                 | 276 ms: 1.01x faster                                                       |
| asyncio_websockets      | 567 ms                                                                 | 564 ms: 1.01x faster                                                       |
| pathlib                 | 17.7 ms                                                                | 17.6 ms: 1.00x faster                                                      |
| regex_v8                | 25.9 ms                                                                | 25.8 ms: 1.00x faster                                                      |
| asyncio_tcp             | 510 ms                                                                 | 512 ms: 1.00x slower                                                       |
| asyncio_tcp_ssl         | 1.85 sec                                                               | 1.86 sec: 1.00x slower                                                     |
| json_loads              | 27.7 us                                                                | 27.8 us: 1.00x slower                                                      |
| pickle_dict             | 33.9 us                                                                | 34.1 us: 1.00x slower                                                      |
| sympy_expand            | 494 ms                                                                 | 496 ms: 1.00x slower                                                       |
| bench_thread_pool       | 860 us                                                                 | 864 us: 1.00x slower                                                       |
| python_startup          | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| thrift                  | 819 us                                                                 | 825 us: 1.01x slower                                                       |
| xml_etree_parse         | 159 ms                                                                 | 161 ms: 1.01x slower                                                       |
| python_startup_no_site  | 7.59 ms                                                                | 7.66 ms: 1.01x slower                                                      |
| html5lib                | 67.2 ms                                                                | 67.9 ms: 1.01x slower                                                      |
| logging_silent          | 101 ns                                                                 | 103 ns: 1.02x slower                                                       |
| deepcopy_memo           | 38.6 us                                                                | 39.3 us: 1.02x slower                                                      |
| async_generators        | 462 ms                                                                 | 471 ms: 1.02x slower                                                       |
| chameleon               | 6.94 ms                                                                | 7.12 ms: 1.03x slower                                                      |
| regex_effbot            | 3.67 ms                                                                | 3.77 ms: 1.03x slower                                                      |
| gc_traversal            | 3.79 ms                                                                | 4.00 ms: 1.06x slower                                                      |
| Geometric mean          | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (30): async_tree_none_tg, richards, genshi_xml, async_tree_memoization_tg, dulwich_log, sympy_integrate, async_tree_memoization, logging_format, deepcopy, docutils, tornado_http, typing_runtime_protocols, aiohttp, pylint, coroutines, async_tree_io, deepcopy_reduce, async_tree_cpu_io_mixed, gunicorn, mypy2, pickle_pure_python, pycparser, dask, async_tree_cpu_io_mixed_tg, bench_mp_pool, sympy_sum, async_tree_io_tg, async_tree_none, deltablue, djangocms

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x
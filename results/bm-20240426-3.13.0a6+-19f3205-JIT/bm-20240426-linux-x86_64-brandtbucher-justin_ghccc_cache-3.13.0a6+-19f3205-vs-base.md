# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 19f3205
- commit date: 2024-04-26
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 276 ms: 1.01x faster                                                       |
| chameleon      | 7.11 ms                                                                | 6.99 ms: 1.02x faster                                                      |
| docutils       | 2.91 sec                                                               | 2.92 sec: 1.00x slower                                                     |
| tornado_http   | 95.9 ms                                                                | 96.2 ms: 1.00x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg | 341 ms                                                                 | 336 ms: 1.02x faster                                                       |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io_tg, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 77.8 ms: 1.16x faster                                                      |
| float          | 77.2 ms                                                                | 72.7 ms: 1.06x faster                                                      |
| pidigits       | 189 ms                                                                 | 190 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                                 | 139 ms: 1.02x faster                                                       |
| regex_v8       | 25.2 ms                                                                | 25.3 ms: 1.00x slower                                                      |
| regex_effbot   | 3.67 ms                                                                | 3.73 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.03 sec                                                               | 1.92 sec: 1.06x faster                                                     |
| unpickle_pure_python | 237 us                                                                 | 226 us: 1.05x faster                                                       |
| unpickle             | 15.5 us                                                                | 15.0 us: 1.03x faster                                                      |
| xml_etree_iterparse  | 104 ms                                                                 | 102 ms: 1.02x faster                                                       |
| xml_etree_parse      | 152 ms                                                                 | 149 ms: 1.02x faster                                                       |
| pickle_pure_python   | 308 us                                                                 | 306 us: 1.01x faster                                                       |
| pickle               | 11.6 us                                                                | 11.7 us: 1.01x slower                                                      |
| json_loads           | 27.3 us                                                                | 27.6 us: 1.01x slower                                                      |
| unpickle_list        | 5.16 us                                                                | 5.26 us: 1.02x slower                                                      |
| pickle_dict          | 34.0 us                                                                | 35.4 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (4): pickle_list, xml_etree_generate, xml_etree_process, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| python_startup_no_site | 7.57 ms                                                                | 7.69 ms: 1.02x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.1 ms: 1.07x faster                                                      |
| django_template | 36.4 ms                                                                | 35.8 ms: 1.02x faster                                                      |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody                   | 90.4 ms                                                                | 77.8 ms: 1.16x faster                                                      |
| spectral_norm           | 114 ms                                                                 | 97.9 ms: 1.16x faster                                                      |
| scimark_sparse_mat_mult | 4.96 ms                                                                | 4.33 ms: 1.15x faster                                                      |
| scimark_fft             | 344 ms                                                                 | 303 ms: 1.13x faster                                                       |
| scimark_monte_carlo     | 70.0 ms                                                                | 63.6 ms: 1.10x faster                                                      |
| fannkuch                | 386 ms                                                                 | 353 ms: 1.09x faster                                                       |
| crypto_pyaes            | 73.3 ms                                                                | 68.3 ms: 1.07x faster                                                      |
| mako                    | 10.8 ms                                                                | 10.1 ms: 1.07x faster                                                      |
| float                   | 77.2 ms                                                                | 72.7 ms: 1.06x faster                                                      |
| tomli_loads             | 2.03 sec                                                               | 1.92 sec: 1.06x faster                                                     |
| hexiom                  | 6.88 ms                                                                | 6.53 ms: 1.05x faster                                                      |
| pprint_pformat          | 1.55 sec                                                               | 1.47 sec: 1.05x faster                                                     |
| chaos                   | 63.4 ms                                                                | 60.3 ms: 1.05x faster                                                      |
| unpickle_pure_python    | 237 us                                                                 | 226 us: 1.05x faster                                                       |
| pprint_safe_repr        | 763 ms                                                                 | 728 ms: 1.05x faster                                                       |
| nqueens                 | 89.8 ms                                                                | 85.7 ms: 1.05x faster                                                      |
| logging_silent          | 108 ns                                                                 | 103 ns: 1.05x faster                                                       |
| richards                | 43.7 ms                                                                | 41.9 ms: 1.04x faster                                                      |
| scimark_lu              | 132 ms                                                                 | 127 ms: 1.04x faster                                                       |
| go                      | 155 ms                                                                 | 149 ms: 1.04x faster                                                       |
| scimark_sor             | 134 ms                                                                 | 130 ms: 1.04x faster                                                       |
| gc_traversal            | 4.01 ms                                                                | 3.87 ms: 1.04x faster                                                      |
| pyflate                 | 463 ms                                                                 | 448 ms: 1.03x faster                                                       |
| unpickle                | 15.5 us                                                                | 15.0 us: 1.03x faster                                                      |
| comprehensions          | 17.7 us                                                                | 17.2 us: 1.03x faster                                                      |
| richards_super          | 49.4 ms                                                                | 48.4 ms: 1.02x faster                                                      |
| xml_etree_iterparse     | 104 ms                                                                 | 102 ms: 1.02x faster                                                       |
| xml_etree_parse         | 152 ms                                                                 | 149 ms: 1.02x faster                                                       |
| pycparser               | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                     |
| chameleon               | 7.11 ms                                                                | 6.99 ms: 1.02x faster                                                      |
| django_template         | 36.4 ms                                                                | 35.8 ms: 1.02x faster                                                      |
| async_tree_none_tg      | 341 ms                                                                 | 336 ms: 1.02x faster                                                       |
| regex_compile           | 141 ms                                                                 | 139 ms: 1.02x faster                                                       |
| json                    | 5.10 ms                                                                | 5.04 ms: 1.01x faster                                                      |
| telco                   | 8.73 ms                                                                | 8.63 ms: 1.01x faster                                                      |
| sqlglot_transpile       | 1.65 ms                                                                | 1.64 ms: 1.01x faster                                                      |
| pickle_pure_python      | 308 us                                                                 | 306 us: 1.01x faster                                                       |
| sqlite_synth            | 2.86 us                                                                | 2.85 us: 1.01x faster                                                      |
| sympy_sum               | 168 ms                                                                 | 167 ms: 1.01x faster                                                       |
| 2to3                    | 277 ms                                                                 | 276 ms: 1.01x faster                                                       |
| asyncio_websockets      | 566 ms                                                                 | 564 ms: 1.00x faster                                                       |
| asyncio_tcp_ssl         | 1.86 sec                                                               | 1.85 sec: 1.00x faster                                                     |
| pidigits                | 189 ms                                                                 | 190 ms: 1.00x slower                                                       |
| tornado_http            | 95.9 ms                                                                | 96.2 ms: 1.00x slower                                                      |
| docutils                | 2.91 sec                                                               | 2.92 sec: 1.00x slower                                                     |
| regex_v8                | 25.2 ms                                                                | 25.3 ms: 1.00x slower                                                      |
| pathlib                 | 17.6 ms                                                                | 17.7 ms: 1.00x slower                                                      |
| bench_mp_pool           | 24.0 ms                                                                | 24.1 ms: 1.01x slower                                                      |
| sqlglot_normalize       | 113 ms                                                                 | 113 ms: 1.01x slower                                                       |
| sympy_expand            | 494 ms                                                                 | 497 ms: 1.01x slower                                                       |
| coverage                | 96.7 ms                                                                | 97.4 ms: 1.01x slower                                                      |
| pickle                  | 11.6 us                                                                | 11.7 us: 1.01x slower                                                      |
| bench_thread_pool       | 859 us                                                                 | 866 us: 1.01x slower                                                       |
| async_generators        | 462 ms                                                                 | 467 ms: 1.01x slower                                                       |
| json_loads              | 27.3 us                                                                | 27.6 us: 1.01x slower                                                      |
| coroutines              | 22.6 ms                                                                | 22.9 ms: 1.01x slower                                                      |
| python_startup          | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| asyncio_tcp             | 509 ms                                                                 | 516 ms: 1.01x slower                                                       |
| regex_effbot            | 3.67 ms                                                                | 3.73 ms: 1.02x slower                                                      |
| python_startup_no_site  | 7.57 ms                                                                | 7.69 ms: 1.02x slower                                                      |
| unpickle_list           | 5.16 us                                                                | 5.26 us: 1.02x slower                                                      |
| djangocms               | 31.9 us                                                                | 32.6 us: 1.02x slower                                                      |
| mdp                     | 2.68 sec                                                               | 2.77 sec: 1.03x slower                                                     |
| pickle_dict             | 34.0 us                                                                | 35.4 us: 1.04x slower                                                      |
| Geometric mean          | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (37): async_tree_none, async_tree_io_tg, deltablue, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed_tg, dask, async_tree_cpu_io_mixed, genshi_text, html5lib, sympy_str, async_tree_memoization, pylint, sqlglot_optimize, deepcopy_reduce, raytrace, create_gc_cycles, logging_simple, dulwich_log, regex_dna, deepcopy_memo, sympy_integrate, aiohttp, logging_format, sqlglot_parse, generators, typing_runtime_protocols, deepcopy, meteor_contest, thrift, gunicorn, pickle_list, xml_etree_generate, xml_etree_process, mypy2, genshi_xml, json_dumps

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x
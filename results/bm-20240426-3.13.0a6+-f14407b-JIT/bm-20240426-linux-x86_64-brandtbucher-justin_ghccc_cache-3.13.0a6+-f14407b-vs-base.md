# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: f14407b
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 275 ms: 1.01x faster                                                       |
| docutils       | 2.91 sec                                                               | 2.93 sec: 1.01x slower                                                     |
| html5lib       | 68.8 ms                                                                | 68.1 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg | 341 ms                                                                 | 335 ms: 1.02x faster                                                       |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (7): async_tree_io, async_tree_memoization_tg, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 80.0 ms: 1.13x faster                                                      |
| float          | 77.2 ms                                                                | 73.1 ms: 1.06x faster                                                      |
| pidigits       | 189 ms                                                                 | 210 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 230 ms                                                                 | 225 ms: 1.02x faster                                                       |
| regex_v8       | 25.2 ms                                                                | 24.7 ms: 1.02x faster                                                      |
| regex_effbot   | 3.67 ms                                                                | 4.23 ms: 1.15x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.03 sec                                                               | 1.93 sec: 1.05x faster                                                     |
| unpickle_pure_python | 237 us                                                                 | 226 us: 1.05x faster                                                       |
| xml_etree_iterparse  | 104 ms                                                                 | 102 ms: 1.02x faster                                                       |
| xml_etree_parse      | 152 ms                                                                 | 149 ms: 1.02x faster                                                       |
| xml_etree_generate   | 87.3 ms                                                                | 86.8 ms: 1.01x faster                                                      |
| json_loads           | 27.3 us                                                                | 27.4 us: 1.00x slower                                                      |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                      |
| pickle_dict          | 34.0 us                                                                | 34.8 us: 1.02x slower                                                      |
| pickle               | 11.6 us                                                                | 12.0 us: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (5): pickle_list, unpickle_list, pickle_pure_python, xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| python_startup_no_site | 7.57 ms                                                                | 7.66 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.0 ms: 1.08x faster                                                      |
| django_template | 36.4 ms                                                                | 36.7 ms: 1.01x slower                                                      |
| genshi_xml      | 53.7 ms                                                                | 54.1 ms: 1.01x slower                                                      |
| genshi_text     | 24.5 ms                                                                | 25.0 ms: 1.02x slower                                                      |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| spectral_norm           | 114 ms                                                                 | 99.2 ms: 1.14x faster                                                      |
| nbody                   | 90.4 ms                                                                | 80.0 ms: 1.13x faster                                                      |
| scimark_monte_carlo     | 70.0 ms                                                                | 62.5 ms: 1.12x faster                                                      |
| scimark_fft             | 344 ms                                                                 | 310 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult | 4.96 ms                                                                | 4.55 ms: 1.09x faster                                                      |
| crypto_pyaes            | 73.3 ms                                                                | 67.6 ms: 1.08x faster                                                      |
| fannkuch                | 386 ms                                                                 | 357 ms: 1.08x faster                                                       |
| mako                    | 10.8 ms                                                                | 10.0 ms: 1.08x faster                                                      |
| pyflate                 | 463 ms                                                                 | 434 ms: 1.07x faster                                                       |
| pprint_pformat          | 1.55 sec                                                               | 1.46 sec: 1.06x faster                                                     |
| pprint_safe_repr        | 763 ms                                                                 | 722 ms: 1.06x faster                                                       |
| float                   | 77.2 ms                                                                | 73.1 ms: 1.06x faster                                                      |
| go                      | 155 ms                                                                 | 147 ms: 1.05x faster                                                       |
| scimark_lu              | 132 ms                                                                 | 125 ms: 1.05x faster                                                       |
| tomli_loads             | 2.03 sec                                                               | 1.93 sec: 1.05x faster                                                     |
| scimark_sor             | 134 ms                                                                 | 128 ms: 1.05x faster                                                       |
| hexiom                  | 6.88 ms                                                                | 6.57 ms: 1.05x faster                                                      |
| unpickle_pure_python    | 237 us                                                                 | 226 us: 1.05x faster                                                       |
| gc_traversal            | 4.01 ms                                                                | 3.86 ms: 1.04x faster                                                      |
| chaos                   | 63.4 ms                                                                | 61.0 ms: 1.04x faster                                                      |
| logging_silent          | 108 ns                                                                 | 104 ns: 1.04x faster                                                       |
| richards                | 43.7 ms                                                                | 42.4 ms: 1.03x faster                                                      |
| comprehensions          | 17.7 us                                                                | 17.2 us: 1.03x faster                                                      |
| nqueens                 | 89.8 ms                                                                | 87.5 ms: 1.03x faster                                                      |
| pycparser               | 1.19 sec                                                               | 1.16 sec: 1.03x faster                                                     |
| regex_dna               | 230 ms                                                                 | 225 ms: 1.02x faster                                                       |
| xml_etree_iterparse     | 104 ms                                                                 | 102 ms: 1.02x faster                                                       |
| regex_v8                | 25.2 ms                                                                | 24.7 ms: 1.02x faster                                                      |
| async_tree_none_tg      | 341 ms                                                                 | 335 ms: 1.02x faster                                                       |
| xml_etree_parse         | 152 ms                                                                 | 149 ms: 1.02x faster                                                       |
| generators              | 30.3 ms                                                                | 29.8 ms: 1.02x faster                                                      |
| sqlglot_transpile       | 1.65 ms                                                                | 1.63 ms: 1.01x faster                                                      |
| sqlite_synth            | 2.86 us                                                                | 2.83 us: 1.01x faster                                                      |
| sqlglot_parse           | 1.32 ms                                                                | 1.31 ms: 1.01x faster                                                      |
| richards_super          | 49.4 ms                                                                | 48.9 ms: 1.01x faster                                                      |
| create_gc_cycles        | 1.77 ms                                                                | 1.75 ms: 1.01x faster                                                      |
| html5lib                | 68.8 ms                                                                | 68.1 ms: 1.01x faster                                                      |
| meteor_contest          | 111 ms                                                                 | 110 ms: 1.01x faster                                                       |
| 2to3                    | 277 ms                                                                 | 275 ms: 1.01x faster                                                       |
| sympy_sum               | 168 ms                                                                 | 166 ms: 1.01x faster                                                       |
| deepcopy_reduce         | 3.22 us                                                                | 3.20 us: 1.01x faster                                                      |
| xml_etree_generate      | 87.3 ms                                                                | 86.8 ms: 1.01x faster                                                      |
| sympy_str               | 295 ms                                                                 | 294 ms: 1.00x faster                                                       |
| sympy_integrate         | 22.0 ms                                                                | 21.9 ms: 1.00x faster                                                      |
| asyncio_websockets      | 566 ms                                                                 | 564 ms: 1.00x faster                                                       |
| asyncio_tcp_ssl         | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                     |
| sympy_expand            | 494 ms                                                                 | 496 ms: 1.00x slower                                                       |
| bench_thread_pool       | 859 us                                                                 | 863 us: 1.00x slower                                                       |
| sqlglot_normalize       | 113 ms                                                                 | 113 ms: 1.00x slower                                                       |
| json_loads              | 27.3 us                                                                | 27.4 us: 1.00x slower                                                      |
| dulwich_log             | 69.3 ms                                                                | 69.7 ms: 1.01x slower                                                      |
| logging_format          | 6.47 us                                                                | 6.52 us: 1.01x slower                                                      |
| django_template         | 36.4 ms                                                                | 36.7 ms: 1.01x slower                                                      |
| asyncio_tcp             | 509 ms                                                                 | 513 ms: 1.01x slower                                                       |
| genshi_xml              | 53.7 ms                                                                | 54.1 ms: 1.01x slower                                                      |
| python_startup          | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| docutils                | 2.91 sec                                                               | 2.93 sec: 1.01x slower                                                     |
| coroutines              | 22.6 ms                                                                | 22.8 ms: 1.01x slower                                                      |
| json_dumps              | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                      |
| python_startup_no_site  | 7.57 ms                                                                | 7.66 ms: 1.01x slower                                                      |
| thrift                  | 823 us                                                                 | 834 us: 1.01x slower                                                       |
| pathlib                 | 17.6 ms                                                                | 17.9 ms: 1.01x slower                                                      |
| coverage                | 96.7 ms                                                                | 98.1 ms: 1.01x slower                                                      |
| deepcopy_memo           | 39.2 us                                                                | 39.8 us: 1.01x slower                                                      |
| async_generators        | 462 ms                                                                 | 470 ms: 1.02x slower                                                       |
| logging_simple          | 5.81 us                                                                | 5.92 us: 1.02x slower                                                      |
| genshi_text             | 24.5 ms                                                                | 25.0 ms: 1.02x slower                                                      |
| pickle_dict             | 34.0 us                                                                | 34.8 us: 1.02x slower                                                      |
| pickle                  | 11.6 us                                                                | 12.0 us: 1.03x slower                                                      |
| mdp                     | 2.68 sec                                                               | 2.79 sec: 1.04x slower                                                     |
| pidigits                | 189 ms                                                                 | 210 ms: 1.11x slower                                                       |
| regex_effbot            | 3.67 ms                                                                | 4.23 ms: 1.15x slower                                                      |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (29): async_tree_io, async_tree_memoization_tg, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, dask, chameleon, async_tree_cpu_io_mixed, pylint, deltablue, pickle_list, unpickle_list, tornado_http, sqlglot_optimize, pickle_pure_python, regex_compile, typing_runtime_protocols, xml_etree_process, aiohttp, bench_mp_pool, telco, async_tree_memoization, deepcopy, mypy2, raytrace, gunicorn, unpickle, json, djangocms

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x
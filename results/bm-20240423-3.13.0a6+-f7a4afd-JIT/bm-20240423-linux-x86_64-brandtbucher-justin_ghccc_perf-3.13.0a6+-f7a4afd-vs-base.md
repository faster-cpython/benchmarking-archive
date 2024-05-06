# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_perf
- machine: linux-x86_64
- commit hash: f7a4afd
- commit date: 2024-04-23
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 275 ms: 1.01x faster                                                      |
| chameleon      | 7.11 ms                                                                | 7.00 ms: 1.02x faster                                                     |
| html5lib       | 68.8 ms                                                                | 68.2 ms: 1.01x faster                                                     |
| tornado_http   | 95.9 ms                                                                | 95.7 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 82.4 ms: 1.10x faster                                                     |
| float          | 77.2 ms                                                                | 74.9 ms: 1.03x faster                                                     |
| pidigits       | 189 ms                                                                 | 192 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 25.2 ms                                                                | 24.6 ms: 1.03x faster                                                     |
| regex_dna      | 230 ms                                                                 | 225 ms: 1.02x faster                                                      |
| regex_compile  | 141 ms                                                                 | 140 ms: 1.01x faster                                                      |
| regex_effbot   | 3.67 ms                                                                | 3.80 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_pure_python | 237 us                                                                 | 227 us: 1.04x faster                                                      |
| tomli_loads          | 2.03 sec                                                               | 1.96 sec: 1.04x faster                                                    |
| unpickle             | 15.5 us                                                                | 15.2 us: 1.02x faster                                                     |
| xml_etree_iterparse  | 104 ms                                                                 | 103 ms: 1.01x faster                                                      |
| xml_etree_generate   | 87.3 ms                                                                | 86.7 ms: 1.01x faster                                                     |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                     |
| pickle_pure_python   | 308 us                                                                 | 307 us: 1.00x faster                                                      |
| pickle               | 11.6 us                                                                | 11.7 us: 1.01x slower                                                     |
| pickle_dict          | 34.0 us                                                                | 34.4 us: 1.01x slower                                                     |
| pickle_list          | 5.11 us                                                                | 5.17 us: 1.01x slower                                                     |
| json_loads           | 27.3 us                                                                | 28.3 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_process, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                     |
| python_startup_no_site | 7.57 ms                                                                | 7.60 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 10.8 ms                                                                | 10.1 ms: 1.08x faster                                                     |
| genshi_text    | 24.5 ms                                                                | 24.6 ms: 1.01x slower                                                     |
| genshi_xml     | 53.7 ms                                                                | 54.5 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| spectral_norm            | 114 ms                                                                 | 97.8 ms: 1.16x faster                                                     |
| nbody                    | 90.4 ms                                                                | 82.4 ms: 1.10x faster                                                     |
| scimark_fft              | 344 ms                                                                 | 315 ms: 1.09x faster                                                      |
| scimark_monte_carlo      | 70.0 ms                                                                | 64.2 ms: 1.09x faster                                                     |
| mako                     | 10.8 ms                                                                | 10.1 ms: 1.08x faster                                                     |
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.62 ms: 1.07x faster                                                     |
| logging_silent           | 108 ns                                                                 | 101 ns: 1.06x faster                                                      |
| fannkuch                 | 386 ms                                                                 | 364 ms: 1.06x faster                                                      |
| gc_traversal             | 4.01 ms                                                                | 3.80 ms: 1.06x faster                                                     |
| crypto_pyaes             | 73.3 ms                                                                | 69.6 ms: 1.05x faster                                                     |
| scimark_sor              | 134 ms                                                                 | 128 ms: 1.05x faster                                                      |
| typing_runtime_protocols | 117 us                                                                 | 112 us: 1.05x faster                                                      |
| hexiom                   | 6.88 ms                                                                | 6.58 ms: 1.05x faster                                                     |
| unpickle_pure_python     | 237 us                                                                 | 227 us: 1.04x faster                                                      |
| chaos                    | 63.4 ms                                                                | 60.7 ms: 1.04x faster                                                     |
| pyflate                  | 463 ms                                                                 | 444 ms: 1.04x faster                                                      |
| tomli_loads              | 2.03 sec                                                               | 1.96 sec: 1.04x faster                                                    |
| comprehensions           | 17.7 us                                                                | 17.1 us: 1.03x faster                                                     |
| richards                 | 43.7 ms                                                                | 42.3 ms: 1.03x faster                                                     |
| float                    | 77.2 ms                                                                | 74.9 ms: 1.03x faster                                                     |
| scimark_lu               | 132 ms                                                                 | 128 ms: 1.03x faster                                                      |
| pprint_safe_repr         | 763 ms                                                                 | 741 ms: 1.03x faster                                                      |
| pprint_pformat           | 1.55 sec                                                               | 1.51 sec: 1.03x faster                                                    |
| regex_v8                 | 25.2 ms                                                                | 24.6 ms: 1.03x faster                                                     |
| regex_dna                | 230 ms                                                                 | 225 ms: 1.02x faster                                                      |
| nqueens                  | 89.8 ms                                                                | 87.9 ms: 1.02x faster                                                     |
| pycparser                | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                    |
| unpickle                 | 15.5 us                                                                | 15.2 us: 1.02x faster                                                     |
| coroutines               | 22.6 ms                                                                | 22.2 ms: 1.02x faster                                                     |
| chameleon                | 7.11 ms                                                                | 7.00 ms: 1.02x faster                                                     |
| generators               | 30.3 ms                                                                | 29.8 ms: 1.01x faster                                                     |
| meteor_contest           | 111 ms                                                                 | 109 ms: 1.01x faster                                                      |
| xml_etree_iterparse      | 104 ms                                                                 | 103 ms: 1.01x faster                                                      |
| richards_super           | 49.4 ms                                                                | 48.9 ms: 1.01x faster                                                     |
| sympy_sum                | 168 ms                                                                 | 166 ms: 1.01x faster                                                      |
| deepcopy_memo            | 39.2 us                                                                | 38.8 us: 1.01x faster                                                     |
| html5lib                 | 68.8 ms                                                                | 68.2 ms: 1.01x faster                                                     |
| xml_etree_generate       | 87.3 ms                                                                | 86.7 ms: 1.01x faster                                                     |
| sympy_integrate          | 22.0 ms                                                                | 21.9 ms: 1.01x faster                                                     |
| bench_thread_pool        | 859 us                                                                 | 853 us: 1.01x faster                                                      |
| 2to3                     | 277 ms                                                                 | 275 ms: 1.01x faster                                                      |
| sqlglot_transpile        | 1.65 ms                                                                | 1.64 ms: 1.01x faster                                                     |
| dulwich_log              | 69.3 ms                                                                | 68.9 ms: 1.01x faster                                                     |
| regex_compile            | 141 ms                                                                 | 140 ms: 1.01x faster                                                      |
| json_dumps               | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                     |
| sympy_str                | 295 ms                                                                 | 293 ms: 1.00x faster                                                      |
| raytrace                 | 273 ms                                                                 | 272 ms: 1.00x faster                                                      |
| pickle_pure_python       | 308 us                                                                 | 307 us: 1.00x faster                                                      |
| deepcopy                 | 361 us                                                                 | 360 us: 1.00x faster                                                      |
| tornado_http             | 95.9 ms                                                                | 95.7 ms: 1.00x faster                                                     |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                    |
| create_gc_cycles         | 1.77 ms                                                                | 1.77 ms: 1.00x slower                                                     |
| python_startup           | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                     |
| python_startup_no_site   | 7.57 ms                                                                | 7.60 ms: 1.00x slower                                                     |
| sqlglot_normalize        | 113 ms                                                                 | 113 ms: 1.01x slower                                                      |
| genshi_text              | 24.5 ms                                                                | 24.6 ms: 1.01x slower                                                     |
| async_generators         | 462 ms                                                                 | 465 ms: 1.01x slower                                                      |
| asyncio_tcp              | 509 ms                                                                 | 513 ms: 1.01x slower                                                      |
| thrift                   | 823 us                                                                 | 830 us: 1.01x slower                                                      |
| json                     | 5.10 ms                                                                | 5.15 ms: 1.01x slower                                                     |
| pickle                   | 11.6 us                                                                | 11.7 us: 1.01x slower                                                     |
| pathlib                  | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                     |
| pickle_dict              | 34.0 us                                                                | 34.4 us: 1.01x slower                                                     |
| pickle_list              | 5.11 us                                                                | 5.17 us: 1.01x slower                                                     |
| logging_format           | 6.47 us                                                                | 6.56 us: 1.02x slower                                                     |
| pidigits                 | 189 ms                                                                 | 192 ms: 1.02x slower                                                      |
| genshi_xml               | 53.7 ms                                                                | 54.5 ms: 1.02x slower                                                     |
| coverage                 | 96.7 ms                                                                | 98.6 ms: 1.02x slower                                                     |
| logging_simple           | 5.81 us                                                                | 5.94 us: 1.02x slower                                                     |
| regex_effbot             | 3.67 ms                                                                | 3.80 ms: 1.04x slower                                                     |
| json_loads               | 27.3 us                                                                | 28.3 us: 1.04x slower                                                     |
| mdp                      | 2.68 sec                                                               | 2.84 sec: 1.06x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (29): deltablue, async_tree_io_tg, dask, async_tree_memoization, async_tree_io, xml_etree_parse, telco, go, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, sqlglot_parse, bench_mp_pool, sqlite_synth, pylint, mypy2, xml_etree_process, aiohttp, asyncio_websockets, sqlglot_optimize, deepcopy_reduce, async_tree_memoization_tg, gunicorn, sympy_expand, docutils, unpickle_list, djangocms, django_template

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: 07e95c4
- commit date: 2024-04-23
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 275 ms: 1.01x faster                                                 |
| chameleon      | 7.11 ms                                                                | 6.93 ms: 1.03x faster                                                |
| html5lib       | 68.8 ms                                                                | 67.8 ms: 1.02x faster                                                |
| tornado_http   | 95.9 ms                                                                | 96.3 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg | 341 ms                                                                 | 336 ms: 1.02x faster                                                 |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_io, async_tree_none, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 82.2 ms: 1.10x faster                                                |
| float          | 77.2 ms                                                                | 73.4 ms: 1.05x faster                                                |
| pidigits       | 189 ms                                                                 | 197 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 230 ms                                                                 | 218 ms: 1.06x faster                                                 |
| regex_v8       | 25.2 ms                                                                | 24.4 ms: 1.03x faster                                                |
| regex_effbot   | 3.67 ms                                                                | 3.57 ms: 1.03x faster                                                |
| regex_compile  | 141 ms                                                                 | 140 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                                | 4.75 us: 1.07x faster                                                |
| unpickle_pure_python | 237 us                                                                 | 227 us: 1.04x faster                                                 |
| tomli_loads          | 2.03 sec                                                               | 1.96 sec: 1.04x faster                                               |
| xml_etree_iterparse  | 104 ms                                                                 | 102 ms: 1.02x faster                                                 |
| unpickle_list        | 5.16 us                                                                | 5.05 us: 1.02x faster                                                |
| pickle_dict          | 34.0 us                                                                | 33.5 us: 1.01x faster                                                |
| pickle_pure_python   | 308 us                                                                 | 305 us: 1.01x faster                                                 |
| json_loads           | 27.3 us                                                                | 27.6 us: 1.01x slower                                                |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                |
| pickle               | 11.6 us                                                                | 11.9 us: 1.02x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_generate, xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 9.96 ms: 1.09x faster                                                |
| django_template | 36.4 ms                                                                | 36.2 ms: 1.00x faster                                                |
| genshi_text     | 24.5 ms                                                                | 24.7 ms: 1.01x slower                                                |
| genshi_xml      | 53.7 ms                                                                | 55.4 ms: 1.03x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| spectral_norm            | 114 ms                                                                 | 98.9 ms: 1.15x faster                                                |
| nbody                    | 90.4 ms                                                                | 82.2 ms: 1.10x faster                                                |
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.52 ms: 1.10x faster                                                |
| scimark_monte_carlo      | 70.0 ms                                                                | 63.9 ms: 1.09x faster                                                |
| fannkuch                 | 386 ms                                                                 | 353 ms: 1.09x faster                                                 |
| scimark_fft              | 344 ms                                                                 | 316 ms: 1.09x faster                                                 |
| mako                     | 10.8 ms                                                                | 9.96 ms: 1.09x faster                                                |
| pickle_list              | 5.11 us                                                                | 4.75 us: 1.07x faster                                                |
| crypto_pyaes             | 73.3 ms                                                                | 68.6 ms: 1.07x faster                                                |
| gc_traversal             | 4.01 ms                                                                | 3.79 ms: 1.06x faster                                                |
| hexiom                   | 6.88 ms                                                                | 6.50 ms: 1.06x faster                                                |
| regex_dna                | 230 ms                                                                 | 218 ms: 1.06x faster                                                 |
| float                    | 77.2 ms                                                                | 73.4 ms: 1.05x faster                                                |
| pyflate                  | 463 ms                                                                 | 442 ms: 1.05x faster                                                 |
| scimark_lu               | 132 ms                                                                 | 126 ms: 1.05x faster                                                 |
| unpickle_pure_python     | 237 us                                                                 | 227 us: 1.04x faster                                                 |
| chaos                    | 63.4 ms                                                                | 60.9 ms: 1.04x faster                                                |
| comprehensions           | 17.7 us                                                                | 17.0 us: 1.04x faster                                                |
| nqueens                  | 89.8 ms                                                                | 86.4 ms: 1.04x faster                                                |
| logging_silent           | 108 ns                                                                 | 104 ns: 1.04x faster                                                 |
| tomli_loads              | 2.03 sec                                                               | 1.96 sec: 1.04x faster                                               |
| regex_v8                 | 25.2 ms                                                                | 24.4 ms: 1.03x faster                                                |
| scimark_sor              | 134 ms                                                                 | 130 ms: 1.03x faster                                                 |
| regex_effbot             | 3.67 ms                                                                | 3.57 ms: 1.03x faster                                                |
| richards                 | 43.7 ms                                                                | 42.5 ms: 1.03x faster                                                |
| typing_runtime_protocols | 117 us                                                                 | 114 us: 1.03x faster                                                 |
| chameleon                | 7.11 ms                                                                | 6.93 ms: 1.03x faster                                                |
| pprint_safe_repr         | 763 ms                                                                 | 745 ms: 1.02x faster                                                 |
| xml_etree_iterparse      | 104 ms                                                                 | 102 ms: 1.02x faster                                                 |
| unpickle_list            | 5.16 us                                                                | 5.05 us: 1.02x faster                                                |
| deepcopy_memo            | 39.2 us                                                                | 38.5 us: 1.02x faster                                                |
| async_tree_none_tg       | 341 ms                                                                 | 336 ms: 1.02x faster                                                 |
| html5lib                 | 68.8 ms                                                                | 67.8 ms: 1.02x faster                                                |
| meteor_contest           | 111 ms                                                                 | 109 ms: 1.01x faster                                                 |
| richards_super           | 49.4 ms                                                                | 48.8 ms: 1.01x faster                                                |
| pickle_dict              | 34.0 us                                                                | 33.5 us: 1.01x faster                                                |
| deepcopy_reduce          | 3.22 us                                                                | 3.18 us: 1.01x faster                                                |
| go                       | 155 ms                                                                 | 153 ms: 1.01x faster                                                 |
| pickle_pure_python       | 308 us                                                                 | 305 us: 1.01x faster                                                 |
| raytrace                 | 273 ms                                                                 | 271 ms: 1.01x faster                                                 |
| 2to3                     | 277 ms                                                                 | 275 ms: 1.01x faster                                                 |
| sqlglot_transpile        | 1.65 ms                                                                | 1.64 ms: 1.01x faster                                                |
| deepcopy                 | 361 us                                                                 | 358 us: 1.01x faster                                                 |
| regex_compile            | 141 ms                                                                 | 140 ms: 1.01x faster                                                 |
| sqlite_synth             | 2.86 us                                                                | 2.84 us: 1.01x faster                                                |
| sympy_sum                | 168 ms                                                                 | 167 ms: 1.00x faster                                                 |
| django_template          | 36.4 ms                                                                | 36.2 ms: 1.00x faster                                                |
| create_gc_cycles         | 1.77 ms                                                                | 1.76 ms: 1.00x faster                                                |
| sqlglot_optimize         | 57.2 ms                                                                | 57.4 ms: 1.00x slower                                                |
| tornado_http             | 95.9 ms                                                                | 96.3 ms: 1.00x slower                                                |
| logging_simple           | 5.81 us                                                                | 5.86 us: 1.01x slower                                                |
| logging_format           | 6.47 us                                                                | 6.52 us: 1.01x slower                                                |
| sqlglot_normalize        | 113 ms                                                                 | 114 ms: 1.01x slower                                                 |
| asyncio_tcp              | 509 ms                                                                 | 513 ms: 1.01x slower                                                 |
| pathlib                  | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                |
| genshi_text              | 24.5 ms                                                                | 24.7 ms: 1.01x slower                                                |
| json_loads               | 27.3 us                                                                | 27.6 us: 1.01x slower                                                |
| json_dumps               | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                |
| async_generators         | 462 ms                                                                 | 469 ms: 1.01x slower                                                 |
| coroutines               | 22.6 ms                                                                | 22.9 ms: 1.02x slower                                                |
| pickle                   | 11.6 us                                                                | 11.9 us: 1.02x slower                                                |
| mdp                      | 2.68 sec                                                               | 2.76 sec: 1.03x slower                                               |
| genshi_xml               | 53.7 ms                                                                | 55.4 ms: 1.03x slower                                                |
| pidigits                 | 189 ms                                                                 | 197 ms: 1.04x slower                                                 |
| coverage                 | 96.7 ms                                                                | 104 ms: 1.08x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (36): async_tree_io_tg, async_tree_io, async_tree_none, async_tree_memoization_tg, deltablue, async_tree_cpu_io_mixed_tg, pycparser, async_tree_cpu_io_mixed, xml_etree_parse, telco, pprint_pformat, sqlglot_parse, async_tree_memoization, xml_etree_generate, sympy_str, sympy_integrate, dulwich_log, docutils, thrift, asyncio_tcp_ssl, python_startup_no_site, python_startup, dask, djangocms, sympy_expand, xml_etree_process, asyncio_websockets, pylint, bench_thread_pool, bench_mp_pool, unpickle, json, gunicorn, generators, aiohttp, mypy2

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.01x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| chameleon      | 6.96 ms                                                                | 7.05 ms: 1.01x slower                                                |
| tornado_http   | 97.8 ms                                                                | 97.0 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 388 ms                                                                 | 356 ms: 1.09x faster                                                 |
| async_tree_io_tg           | 929 ms                                                                 | 907 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed    | 600 ms                                                                 | 614 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed_tg | 584 ms                                                                 | 599 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 92.8 ms                                                                | 87.0 ms: 1.07x faster                                                |
| float          | 77.0 ms                                                                | 72.8 ms: 1.06x faster                                                |
| pidigits       | 190 ms                                                                 | 189 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.76 ms                                                                | 3.63 ms: 1.04x faster                                                |
| regex_dna      | 226 ms                                                                 | 219 ms: 1.03x faster                                                 |
| regex_v8       | 25.8 ms                                                                | 25.0 ms: 1.03x faster                                                |
| regex_compile  | 147 ms                                                                 | 143 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 5.31 us                                                                | 4.97 us: 1.07x faster                                                |
| unpickle_pure_python | 242 us                                                                 | 229 us: 1.06x faster                                                 |
| tomli_loads          | 2.09 sec                                                               | 2.02 sec: 1.04x faster                                               |
| pickle               | 12.2 us                                                                | 11.8 us: 1.03x faster                                                |
| xml_etree_generate   | 88.9 ms                                                                | 86.7 ms: 1.02x faster                                                |
| xml_etree_process    | 61.0 ms                                                                | 60.0 ms: 1.02x faster                                                |
| unpickle             | 15.3 us                                                                | 15.2 us: 1.01x faster                                                |
| pickle_dict          | 34.5 us                                                                | 34.2 us: 1.01x faster                                                |
| xml_etree_iterparse  | 107 ms                                                                 | 106 ms: 1.01x faster                                                 |
| pickle_pure_python   | 305 us                                                                 | 308 us: 1.01x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                |
| unpickle_list        | 5.16 us                                                                | 5.23 us: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                                |
| python_startup_no_site | 9.53 ms                                                                | 9.49 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 9.96 ms: 1.08x faster                                                |
| genshi_xml      | 55.0 ms                                                                | 55.4 ms: 1.01x slower                                                |
| genshi_text     | 24.5 ms                                                                | 24.9 ms: 1.02x slower                                                |
| django_template | 35.6 ms                                                                | 36.4 ms: 1.02x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| spectral_norm              | 115 ms                                                                 | 101 ms: 1.14x faster                                                 |
| scimark_sparse_mat_mult    | 4.82 ms                                                                | 4.33 ms: 1.11x faster                                                |
| async_tree_none            | 388 ms                                                                 | 356 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 70.4 ms                                                                | 64.9 ms: 1.09x faster                                                |
| pyflate                    | 487 ms                                                                 | 451 ms: 1.08x faster                                                 |
| crypto_pyaes               | 75.6 ms                                                                | 70.1 ms: 1.08x faster                                                |
| mako                       | 10.7 ms                                                                | 9.96 ms: 1.08x faster                                                |
| scimark_fft                | 344 ms                                                                 | 319 ms: 1.08x faster                                                 |
| fannkuch                   | 392 ms                                                                 | 367 ms: 1.07x faster                                                 |
| pickle_list                | 5.31 us                                                                | 4.97 us: 1.07x faster                                                |
| nbody                      | 92.8 ms                                                                | 87.0 ms: 1.07x faster                                                |
| unpickle_pure_python       | 242 us                                                                 | 229 us: 1.06x faster                                                 |
| float                      | 77.0 ms                                                                | 72.8 ms: 1.06x faster                                                |
| comprehensions             | 18.2 us                                                                | 17.4 us: 1.04x faster                                                |
| chaos                      | 62.8 ms                                                                | 60.3 ms: 1.04x faster                                                |
| djangocms                  | 32.6 us                                                                | 31.3 us: 1.04x faster                                                |
| hexiom                     | 7.15 ms                                                                | 6.88 ms: 1.04x faster                                                |
| pycparser                  | 1.24 sec                                                               | 1.19 sec: 1.04x faster                                               |
| regex_effbot               | 3.76 ms                                                                | 3.63 ms: 1.04x faster                                                |
| raytrace                   | 289 ms                                                                 | 279 ms: 1.04x faster                                                 |
| tomli_loads                | 2.09 sec                                                               | 2.02 sec: 1.04x faster                                               |
| regex_dna                  | 226 ms                                                                 | 219 ms: 1.03x faster                                                 |
| regex_v8                   | 25.8 ms                                                                | 25.0 ms: 1.03x faster                                                |
| scimark_lu                 | 134 ms                                                                 | 130 ms: 1.03x faster                                                 |
| pickle                     | 12.2 us                                                                | 11.8 us: 1.03x faster                                                |
| regex_compile              | 147 ms                                                                 | 143 ms: 1.03x faster                                                 |
| xml_etree_generate         | 88.9 ms                                                                | 86.7 ms: 1.02x faster                                                |
| async_tree_io_tg           | 929 ms                                                                 | 907 ms: 1.02x faster                                                 |
| meteor_contest             | 112 ms                                                                 | 109 ms: 1.02x faster                                                 |
| gc_traversal               | 3.77 ms                                                                | 3.69 ms: 1.02x faster                                                |
| richards_super             | 52.8 ms                                                                | 51.7 ms: 1.02x faster                                                |
| xml_etree_process          | 61.0 ms                                                                | 60.0 ms: 1.02x faster                                                |
| sqlite_synth               | 2.89 us                                                                | 2.84 us: 1.01x faster                                                |
| logging_simple             | 6.03 us                                                                | 5.94 us: 1.01x faster                                                |
| sympy_sum                  | 166 ms                                                                 | 164 ms: 1.01x faster                                                 |
| unpickle                   | 15.3 us                                                                | 15.2 us: 1.01x faster                                                |
| pprint_safe_repr           | 746 ms                                                                 | 738 ms: 1.01x faster                                                 |
| generators                 | 30.2 ms                                                                | 29.8 ms: 1.01x faster                                                |
| logging_format             | 6.63 us                                                                | 6.57 us: 1.01x faster                                                |
| pickle_dict                | 34.5 us                                                                | 34.2 us: 1.01x faster                                                |
| richards                   | 46.4 ms                                                                | 46.0 ms: 1.01x faster                                                |
| tornado_http               | 97.8 ms                                                                | 97.0 ms: 1.01x faster                                                |
| xml_etree_iterparse        | 107 ms                                                                 | 106 ms: 1.01x faster                                                 |
| pidigits                   | 190 ms                                                                 | 189 ms: 1.01x faster                                                 |
| coverage                   | 97.3 ms                                                                | 96.9 ms: 1.00x faster                                                |
| dulwich_log                | 71.9 ms                                                                | 71.6 ms: 1.00x faster                                                |
| create_gc_cycles           | 1.67 ms                                                                | 1.66 ms: 1.00x faster                                                |
| sympy_integrate            | 21.8 ms                                                                | 21.7 ms: 1.00x faster                                                |
| python_startup             | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                                |
| python_startup_no_site     | 9.53 ms                                                                | 9.49 ms: 1.00x faster                                                |
| pylint                     | 298 ms                                                                 | 299 ms: 1.00x slower                                                 |
| bench_thread_pool          | 856 us                                                                 | 858 us: 1.00x slower                                                 |
| sqlglot_transpile          | 1.64 ms                                                                | 1.65 ms: 1.00x slower                                                |
| sympy_expand               | 494 ms                                                                 | 497 ms: 1.01x slower                                                 |
| deltablue                  | 3.47 ms                                                                | 3.48 ms: 1.01x slower                                                |
| coroutines                 | 22.3 ms                                                                | 22.4 ms: 1.01x slower                                                |
| genshi_xml                 | 55.0 ms                                                                | 55.4 ms: 1.01x slower                                                |
| logging_silent             | 103 ns                                                                 | 104 ns: 1.01x slower                                                 |
| pickle_pure_python         | 305 us                                                                 | 308 us: 1.01x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                |
| unpickle_list              | 5.16 us                                                                | 5.23 us: 1.01x slower                                                |
| chameleon                  | 6.96 ms                                                                | 7.05 ms: 1.01x slower                                                |
| genshi_text                | 24.5 ms                                                                | 24.9 ms: 1.02x slower                                                |
| json                       | 5.40 ms                                                                | 5.50 ms: 1.02x slower                                                |
| sqlglot_optimize           | 57.6 ms                                                                | 58.7 ms: 1.02x slower                                                |
| deepcopy_reduce            | 3.17 us                                                                | 3.23 us: 1.02x slower                                                |
| django_template            | 35.6 ms                                                                | 36.4 ms: 1.02x slower                                                |
| async_generators           | 458 ms                                                                 | 468 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed    | 600 ms                                                                 | 614 ms: 1.02x slower                                                 |
| scimark_sor                | 133 ms                                                                 | 136 ms: 1.02x slower                                                 |
| deepcopy                   | 355 us                                                                 | 363 us: 1.02x slower                                                 |
| nqueens                    | 89.1 ms                                                                | 91.2 ms: 1.02x slower                                                |
| go                         | 154 ms                                                                 | 158 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed_tg | 584 ms                                                                 | 599 ms: 1.03x slower                                                 |
| typing_runtime_protocols   | 111 us                                                                 | 114 us: 1.03x slower                                                 |
| sqlglot_normalize          | 112 ms                                                                 | 115 ms: 1.03x slower                                                 |
| deepcopy_memo              | 38.7 us                                                                | 40.1 us: 1.03x slower                                                |
| unpack_sequence            | 91.0 ns                                                                | 115 ns: 1.26x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (24): async_tree_memoization, async_tree_io, async_tree_memoization_tg, pprint_pformat, telco, html5lib, aiohttp, sympy_str, docutils, mdp, 2to3, pathlib, dask, xml_etree_parse, gunicorn, asyncio_tcp_ssl, asyncio_websockets, bench_mp_pool, asyncio_tcp, sqlglot_parse, thrift, json_loads, mypy2, async_tree_none_tg

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
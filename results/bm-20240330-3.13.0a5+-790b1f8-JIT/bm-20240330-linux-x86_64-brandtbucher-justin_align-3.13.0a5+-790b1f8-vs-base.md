# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| chameleon      | 7.02 ms                                                                | 7.22 ms: 1.03x slower                                                |
| html5lib       | 68.5 ms                                                                | 66.7 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none | 358 ms                                                                 | 394 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                                | 93.6 ms: 1.01x slower                                                |
| float          | 76.9 ms                                                                | 78.4 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                                | 25.1 ms: 1.03x faster                                                |
| regex_dna      | 226 ms                                                                 | 224 ms: 1.01x faster                                                 |
| regex_effbot   | 3.74 ms                                                                | 3.82 ms: 1.02x slower                                                |
| regex_compile  | 146 ms                                                                 | 153 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_list        | 5.46 us                                                                | 5.21 us: 1.05x faster                                                |
| pickle_dict          | 34.5 us                                                                | 34.1 us: 1.01x faster                                                |
| pickle_pure_python   | 309 us                                                                 | 306 us: 1.01x faster                                                 |
| pickle_list          | 4.99 us                                                                | 4.96 us: 1.01x faster                                                |
| xml_etree_generate   | 88.4 ms                                                                | 88.0 ms: 1.00x faster                                                |
| xml_etree_iterparse  | 107 ms                                                                 | 108 ms: 1.01x slower                                                 |
| json_loads           | 28.5 us                                                                | 28.7 us: 1.01x slower                                                |
| json_dumps           | 10.5 ms                                                                | 10.8 ms: 1.02x slower                                                |
| tomli_loads          | 2.07 sec                                                               | 2.18 sec: 1.05x slower                                               |
| unpickle_pure_python | 238 us                                                                 | 251 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_process, unpickle, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 9.59 ms                                                                | 9.51 ms: 1.01x faster                                                |
| python_startup         | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 35.9 ms                                                                | 36.1 ms: 1.01x slower                                                |
| genshi_xml      | 54.0 ms                                                                | 55.4 ms: 1.03x slower                                                |
| mako            | 10.7 ms                                                                | 11.4 ms: 1.06x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mdp                     | 2.83 sec                                                               | 2.66 sec: 1.06x faster                                               |
| unpickle_list           | 5.46 us                                                                | 5.21 us: 1.05x faster                                                |
| pycparser               | 1.23 sec                                                               | 1.18 sec: 1.04x faster                                               |
| logging_silent          | 103 ns                                                                 | 99.6 ns: 1.03x faster                                                |
| regex_v8                | 26.0 ms                                                                | 25.1 ms: 1.03x faster                                                |
| gc_traversal            | 3.81 ms                                                                | 3.71 ms: 1.03x faster                                                |
| html5lib                | 68.5 ms                                                                | 66.7 ms: 1.03x faster                                                |
| create_gc_cycles        | 1.68 ms                                                                | 1.66 ms: 1.01x faster                                                |
| pickle_dict             | 34.5 us                                                                | 34.1 us: 1.01x faster                                                |
| sqlite_synth            | 2.88 us                                                                | 2.85 us: 1.01x faster                                                |
| python_startup_no_site  | 9.59 ms                                                                | 9.51 ms: 1.01x faster                                                |
| pickle_pure_python      | 309 us                                                                 | 306 us: 1.01x faster                                                 |
| python_startup          | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                |
| regex_dna               | 226 ms                                                                 | 224 ms: 1.01x faster                                                 |
| sqlglot_optimize        | 58.2 ms                                                                | 57.8 ms: 1.01x faster                                                |
| pickle_list             | 4.99 us                                                                | 4.96 us: 1.01x faster                                                |
| aiohttp                 | 1.22 ms                                                                | 1.22 ms: 1.01x faster                                                |
| xml_etree_generate      | 88.4 ms                                                                | 88.0 ms: 1.00x faster                                                |
| bench_thread_pool       | 860 us                                                                 | 857 us: 1.00x faster                                                 |
| asyncio_tcp_ssl         | 1.86 sec                                                               | 1.85 sec: 1.00x faster                                               |
| dulwich_log             | 71.0 ms                                                                | 71.4 ms: 1.01x slower                                                |
| sympy_str               | 292 ms                                                                 | 294 ms: 1.01x slower                                                 |
| sympy_sum               | 166 ms                                                                 | 167 ms: 1.01x slower                                                 |
| xml_etree_iterparse     | 107 ms                                                                 | 108 ms: 1.01x slower                                                 |
| sympy_integrate         | 21.8 ms                                                                | 21.9 ms: 1.01x slower                                                |
| pylint                  | 298 ms                                                                 | 300 ms: 1.01x slower                                                 |
| generators              | 29.9 ms                                                                | 30.1 ms: 1.01x slower                                                |
| json_loads              | 28.5 us                                                                | 28.7 us: 1.01x slower                                                |
| nbody                   | 92.9 ms                                                                | 93.6 ms: 1.01x slower                                                |
| django_template         | 35.9 ms                                                                | 36.1 ms: 1.01x slower                                                |
| logging_format          | 6.50 us                                                                | 6.55 us: 1.01x slower                                                |
| deltablue               | 3.47 ms                                                                | 3.50 ms: 1.01x slower                                                |
| sqlglot_transpile       | 1.64 ms                                                                | 1.66 ms: 1.01x slower                                                |
| meteor_contest          | 111 ms                                                                 | 112 ms: 1.01x slower                                                 |
| thrift                  | 813 us                                                                 | 823 us: 1.01x slower                                                 |
| sympy_expand            | 492 ms                                                                 | 499 ms: 1.01x slower                                                 |
| chaos                   | 63.5 ms                                                                | 64.4 ms: 1.01x slower                                                |
| logging_simple          | 5.88 us                                                                | 5.98 us: 1.02x slower                                                |
| float                   | 76.9 ms                                                                | 78.4 ms: 1.02x slower                                                |
| json_dumps              | 10.5 ms                                                                | 10.8 ms: 1.02x slower                                                |
| regex_effbot            | 3.74 ms                                                                | 3.82 ms: 1.02x slower                                                |
| asyncio_tcp             | 498 ms                                                                 | 510 ms: 1.02x slower                                                 |
| nqueens                 | 91.1 ms                                                                | 93.4 ms: 1.03x slower                                                |
| genshi_xml              | 54.0 ms                                                                | 55.4 ms: 1.03x slower                                                |
| go                      | 155 ms                                                                 | 159 ms: 1.03x slower                                                 |
| scimark_lu              | 131 ms                                                                 | 134 ms: 1.03x slower                                                 |
| chameleon               | 7.02 ms                                                                | 7.22 ms: 1.03x slower                                                |
| scimark_fft             | 344 ms                                                                 | 357 ms: 1.04x slower                                                 |
| scimark_sor             | 129 ms                                                                 | 134 ms: 1.04x slower                                                 |
| richards_super          | 52.5 ms                                                                | 54.6 ms: 1.04x slower                                                |
| pyflate                 | 485 ms                                                                 | 505 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult | 4.89 ms                                                                | 5.09 ms: 1.04x slower                                                |
| scimark_monte_carlo     | 70.1 ms                                                                | 73.3 ms: 1.04x slower                                                |
| fannkuch                | 392 ms                                                                 | 411 ms: 1.05x slower                                                 |
| regex_compile           | 146 ms                                                                 | 153 ms: 1.05x slower                                                 |
| richards                | 46.4 ms                                                                | 48.7 ms: 1.05x slower                                                |
| comprehensions          | 18.3 us                                                                | 19.3 us: 1.05x slower                                                |
| tomli_loads             | 2.07 sec                                                               | 2.18 sec: 1.05x slower                                               |
| unpickle_pure_python    | 238 us                                                                 | 251 us: 1.05x slower                                                 |
| hexiom                  | 7.17 ms                                                                | 7.56 ms: 1.05x slower                                                |
| mako                    | 10.7 ms                                                                | 11.4 ms: 1.06x slower                                                |
| spectral_norm           | 114 ms                                                                 | 121 ms: 1.06x slower                                                 |
| pprint_pformat          | 1.50 sec                                                               | 1.61 sec: 1.08x slower                                               |
| pprint_safe_repr        | 735 ms                                                                 | 798 ms: 1.09x slower                                                 |
| async_tree_none         | 358 ms                                                                 | 394 ms: 1.10x slower                                                 |
| unpack_sequence         | 91.0 ns                                                                | 125 ns: 1.37x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (36): djangocms, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none_tg, typing_runtime_protocols, xml_etree_parse, deepcopy_memo, asyncio_websockets, dask, deepcopy_reduce, coroutines, xml_etree_process, unpickle, tornado_http, sqlglot_normalize, async_generators, pidigits, gunicorn, pickle, docutils, bench_mp_pool, genshi_text, mypy2, deepcopy, coverage, 2to3, pathlib, json, sqlglot_parse, telco, async_tree_io_tg, async_tree_memoization_tg, raytrace, async_tree_memoization, crypto_pyaes, async_tree_io

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x
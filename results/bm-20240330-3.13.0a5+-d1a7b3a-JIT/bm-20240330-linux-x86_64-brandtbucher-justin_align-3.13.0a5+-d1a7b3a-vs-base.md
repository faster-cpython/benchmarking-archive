# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.01x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 276 ms                                                                 | 280 ms: 1.01x slower                                                 |
| chameleon      | 6.96 ms                                                                | 7.00 ms: 1.01x slower                                                |
| tornado_http   | 97.8 ms                                                                | 97.3 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none | 388 ms                                                                 | 392 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 190 ms                                                                 | 189 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 25.8 ms                                                                | 25.6 ms: 1.01x faster                                                |
| regex_dna      | 226 ms                                                                 | 231 ms: 1.02x slower                                                 |
| regex_effbot   | 3.76 ms                                                                | 3.87 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_list        | 5.16 us                                                                | 5.06 us: 1.02x faster                                                |
| unpickle_pure_python | 242 us                                                                 | 240 us: 1.01x faster                                                 |
| json_loads           | 28.6 us                                                                | 28.4 us: 1.01x faster                                                |
| xml_etree_generate   | 88.9 ms                                                                | 89.2 ms: 1.00x slower                                                |
| json_dumps           | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                |
| xml_etree_iterparse  | 107 ms                                                                 | 108 ms: 1.01x slower                                                 |
| tomli_loads          | 2.09 sec                                                               | 2.10 sec: 1.01x slower                                               |
| pickle_list          | 5.31 us                                                                | 5.37 us: 1.01x slower                                                |
| pickle_pure_python   | 305 us                                                                 | 309 us: 1.01x slower                                                 |
| unpickle             | 15.3 us                                                                | 15.6 us: 1.02x slower                                                |
| pickle_dict          | 34.5 us                                                                | 35.3 us: 1.02x slower                                                |
| pickle               | 12.2 us                                                                | 12.5 us: 1.03x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 9.53 ms                                                                | 9.55 ms: 1.00x slower                                                |
| python_startup         | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 35.6 ms                                                                | 35.8 ms: 1.01x slower                                                |
| genshi_text     | 24.5 ms                                                                | 24.6 ms: 1.01x slower                                                |
| mako            | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240329-linux-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpack_sequence          | 91.0 ns                                                                | 87.6 ns: 1.04x faster                                                |
| unpickle_list            | 5.16 us                                                                | 5.06 us: 1.02x faster                                                |
| crypto_pyaes             | 75.6 ms                                                                | 74.4 ms: 1.02x faster                                                |
| json                     | 5.40 ms                                                                | 5.32 ms: 1.02x faster                                                |
| telco                    | 8.61 ms                                                                | 8.48 ms: 1.02x faster                                                |
| logging_simple           | 6.03 us                                                                | 5.94 us: 1.02x faster                                                |
| sympy_sum                | 166 ms                                                                 | 164 ms: 1.02x faster                                                 |
| logging_format           | 6.63 us                                                                | 6.53 us: 1.01x faster                                                |
| unpickle_pure_python     | 242 us                                                                 | 240 us: 1.01x faster                                                 |
| dulwich_log              | 71.9 ms                                                                | 71.2 ms: 1.01x faster                                                |
| logging_silent           | 103 ns                                                                 | 102 ns: 1.01x faster                                                 |
| regex_v8                 | 25.8 ms                                                                | 25.6 ms: 1.01x faster                                                |
| sympy_expand             | 494 ms                                                                 | 491 ms: 1.01x faster                                                 |
| json_loads               | 28.6 us                                                                | 28.4 us: 1.01x faster                                                |
| scimark_lu               | 134 ms                                                                 | 133 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult  | 4.82 ms                                                                | 4.80 ms: 1.01x faster                                                |
| tornado_http             | 97.8 ms                                                                | 97.3 ms: 1.00x faster                                                |
| pidigits                 | 190 ms                                                                 | 189 ms: 1.00x faster                                                 |
| sympy_str                | 292 ms                                                                 | 291 ms: 1.00x faster                                                 |
| scimark_fft              | 344 ms                                                                 | 343 ms: 1.00x faster                                                 |
| python_startup_no_site   | 9.53 ms                                                                | 9.55 ms: 1.00x slower                                                |
| python_startup           | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.86 sec: 1.00x slower                                               |
| xml_etree_generate       | 88.9 ms                                                                | 89.2 ms: 1.00x slower                                                |
| json_dumps               | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                |
| comprehensions           | 18.2 us                                                                | 18.3 us: 1.01x slower                                                |
| django_template          | 35.6 ms                                                                | 35.8 ms: 1.01x slower                                                |
| chameleon                | 6.96 ms                                                                | 7.00 ms: 1.01x slower                                                |
| genshi_text              | 24.5 ms                                                                | 24.6 ms: 1.01x slower                                                |
| sqlglot_optimize         | 57.6 ms                                                                | 58.0 ms: 1.01x slower                                                |
| scimark_monte_carlo      | 70.4 ms                                                                | 70.9 ms: 1.01x slower                                                |
| xml_etree_iterparse      | 107 ms                                                                 | 108 ms: 1.01x slower                                                 |
| bench_mp_pool            | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                                |
| tomli_loads              | 2.09 sec                                                               | 2.10 sec: 1.01x slower                                               |
| richards_super           | 52.8 ms                                                                | 53.3 ms: 1.01x slower                                                |
| async_tree_none          | 388 ms                                                                 | 392 ms: 1.01x slower                                                 |
| mako                     | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                |
| pathlib                  | 19.1 ms                                                                | 19.3 ms: 1.01x slower                                                |
| sqlite_synth             | 2.89 us                                                                | 2.92 us: 1.01x slower                                                |
| 2to3                     | 276 ms                                                                 | 280 ms: 1.01x slower                                                 |
| pyflate                  | 487 ms                                                                 | 493 ms: 1.01x slower                                                 |
| fannkuch                 | 392 ms                                                                 | 397 ms: 1.01x slower                                                 |
| pickle_list              | 5.31 us                                                                | 5.37 us: 1.01x slower                                                |
| sqlglot_transpile        | 1.64 ms                                                                | 1.66 ms: 1.01x slower                                                |
| hexiom                   | 7.15 ms                                                                | 7.24 ms: 1.01x slower                                                |
| create_gc_cycles         | 1.67 ms                                                                | 1.69 ms: 1.01x slower                                                |
| pickle_pure_python       | 305 us                                                                 | 309 us: 1.01x slower                                                 |
| coroutines               | 22.3 ms                                                                | 22.5 ms: 1.01x slower                                                |
| async_generators         | 458 ms                                                                 | 465 ms: 1.02x slower                                                 |
| deltablue                | 3.47 ms                                                                | 3.52 ms: 1.02x slower                                                |
| unpickle                 | 15.3 us                                                                | 15.6 us: 1.02x slower                                                |
| deepcopy_reduce          | 3.17 us                                                                | 3.22 us: 1.02x slower                                                |
| sqlglot_parse            | 1.32 ms                                                                | 1.35 ms: 1.02x slower                                                |
| spectral_norm            | 115 ms                                                                 | 117 ms: 1.02x slower                                                 |
| go                       | 154 ms                                                                 | 157 ms: 1.02x slower                                                 |
| raytrace                 | 289 ms                                                                 | 294 ms: 1.02x slower                                                 |
| regex_dna                | 226 ms                                                                 | 231 ms: 1.02x slower                                                 |
| deepcopy_memo            | 38.7 us                                                                | 39.6 us: 1.02x slower                                                |
| pickle_dict              | 34.5 us                                                                | 35.3 us: 1.02x slower                                                |
| richards                 | 46.4 ms                                                                | 47.5 ms: 1.02x slower                                                |
| pickle                   | 12.2 us                                                                | 12.5 us: 1.03x slower                                                |
| deepcopy                 | 355 us                                                                 | 365 us: 1.03x slower                                                 |
| regex_effbot             | 3.76 ms                                                                | 3.87 ms: 1.03x slower                                                |
| typing_runtime_protocols | 111 us                                                                 | 115 us: 1.03x slower                                                 |
| nqueens                  | 89.1 ms                                                                | 92.7 ms: 1.04x slower                                                |
| gc_traversal             | 3.77 ms                                                                | 3.94 ms: 1.05x slower                                                |
| mdp                      | 2.64 sec                                                               | 2.83 sec: 1.07x slower                                               |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (35): xml_etree_parse, gunicorn, aiohttp, meteor_contest, nbody, async_tree_cpu_io_mixed_tg, generators, coverage, pycparser, regex_compile, sympy_integrate, djangocms, sqlglot_normalize, bench_thread_pool, pprint_safe_repr, async_tree_memoization, docutils, thrift, scimark_sor, mypy2, asyncio_tcp, pprint_pformat, async_tree_memoization_tg, pylint, async_tree_io_tg, asyncio_websockets, float, xml_etree_process, chaos, dask, html5lib, async_tree_cpu_io_mixed, genshi_xml, async_tree_none_tg, async_tree_io

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
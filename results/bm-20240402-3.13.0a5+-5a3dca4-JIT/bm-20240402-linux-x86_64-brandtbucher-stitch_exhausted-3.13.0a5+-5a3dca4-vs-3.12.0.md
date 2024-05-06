# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.01x faster
- HPT reliability: 63.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 282 ms: 1.03x slower                                                     |
| chameleon      | 7.41 ms                                                | 7.06 ms: 1.05x faster                                                    |
| docutils       | 2.77 sec                                               | 2.94 sec: 1.06x slower                                                   |
| tornado_http   | 103 ms                                                 | 96.5 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 907 ms: 1.30x faster                                                     |
| async_tree_none_tg         | 450 ms                                                 | 348 ms: 1.29x faster                                                     |
| async_tree_memoization_tg  | 575 ms                                                 | 449 ms: 1.28x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 458 ms: 1.26x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 928 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 597 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.0 ms: 1.10x faster                                                    |
| nbody          | 97.0 ms                                                | 92.4 ms: 1.05x faster                                                    |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 149 ms: 1.00x slower                                                     |
| regex_effbot   | 3.61 ms                                                | 3.75 ms: 1.04x slower                                                    |
| regex_dna      | 212 ms                                                 | 221 ms: 1.04x slower                                                     |
| regex_v8       | 23.1 ms                                                | 24.7 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.06 sec: 1.13x faster                                                   |
| unpickle             | 15.9 us                                                | 15.0 us: 1.05x faster                                                    |
| pickle_pure_python   | 324 us                                                 | 308 us: 1.05x faster                                                     |
| pickle_dict          | 35.5 us                                                | 34.1 us: 1.04x faster                                                    |
| xml_etree_process    | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                    |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                    |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.02x faster                                                    |
| unpickle_list        | 5.29 us                                                | 5.19 us: 1.02x faster                                                    |
| pickle               | 11.6 us                                                | 11.8 us: 1.01x slower                                                    |
| json_loads           | 28.5 us                                                | 29.0 us: 1.02x slower                                                    |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                    |
| unpickle_pure_python | 230 us                                                 | 238 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                    |
| python_startup_no_site | 6.94 ms                                                | 9.51 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                    |
| django_template | 34.6 ms                                                | 37.1 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.39x faster                                                     |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 907 ms: 1.30x faster                                                     |
| async_tree_none_tg         | 450 ms                                                 | 348 ms: 1.29x faster                                                     |
| async_tree_memoization_tg  | 575 ms                                                 | 449 ms: 1.28x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 458 ms: 1.26x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 928 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 597 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                     |
| comprehensions             | 21.8 us                                                | 18.5 us: 1.18x faster                                                    |
| tomli_loads                | 2.33 sec                                               | 2.06 sec: 1.13x faster                                                   |
| logging_format             | 7.23 us                                                | 6.42 us: 1.13x faster                                                    |
| scimark_fft                | 382 ms                                                 | 343 ms: 1.11x faster                                                     |
| logging_simple             | 6.46 us                                                | 5.84 us: 1.11x faster                                                    |
| float                      | 84.7 ms                                                | 77.0 ms: 1.10x faster                                                    |
| crypto_pyaes               | 81.9 ms                                                | 75.3 ms: 1.09x faster                                                    |
| mako                       | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                    |
| fannkuch                   | 417 ms                                                 | 390 ms: 1.07x faster                                                     |
| deltablue                  | 3.72 ms                                                | 3.48 ms: 1.07x faster                                                    |
| tornado_http               | 103 ms                                                 | 96.5 ms: 1.06x faster                                                    |
| scimark_monte_carlo        | 75.1 ms                                                | 70.8 ms: 1.06x faster                                                    |
| raytrace                   | 312 ms                                                 | 296 ms: 1.05x faster                                                     |
| unpickle                   | 15.9 us                                                | 15.0 us: 1.05x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                | 3.18 us: 1.05x faster                                                    |
| pickle_pure_python         | 324 us                                                 | 308 us: 1.05x faster                                                     |
| chameleon                  | 7.41 ms                                                | 7.06 ms: 1.05x faster                                                    |
| nbody                      | 97.0 ms                                                | 92.4 ms: 1.05x faster                                                    |
| chaos                      | 67.0 ms                                                | 64.1 ms: 1.05x faster                                                    |
| pickle_dict                | 35.5 us                                                | 34.1 us: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.87 ms: 1.04x faster                                                    |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                                    |
| deepcopy_memo              | 40.7 us                                                | 39.3 us: 1.04x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.04x faster                                                    |
| xml_etree_process          | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                    |
| deepcopy                   | 371 us                                                 | 359 us: 1.03x faster                                                     |
| sqlglot_transpile          | 1.68 ms                                                | 1.64 ms: 1.03x faster                                                    |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                    |
| pickle_list                | 5.08 us                                                | 4.96 us: 1.02x faster                                                    |
| unpickle_list              | 5.29 us                                                | 5.19 us: 1.02x faster                                                    |
| logging_silent             | 104 ns                                                 | 103 ns: 1.02x faster                                                     |
| sympy_str                  | 300 ms                                                 | 294 ms: 1.02x faster                                                     |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.01x faster                                                    |
| pathlib                    | 19.3 ms                                                | 19.1 ms: 1.01x faster                                                    |
| async_generators           | 463 ms                                                 | 458 ms: 1.01x faster                                                     |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                     |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                     |
| spectral_norm              | 115 ms                                                 | 114 ms: 1.01x faster                                                     |
| regex_compile              | 148 ms                                                 | 149 ms: 1.00x slower                                                     |
| sqlite_synth               | 2.83 us                                                | 2.86 us: 1.01x slower                                                    |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                     |
| richards                   | 45.8 ms                                                | 46.4 ms: 1.01x slower                                                    |
| pickle                     | 11.6 us                                                | 11.8 us: 1.01x slower                                                    |
| dask                       | 372 ms                                                 | 378 ms: 1.02x slower                                                     |
| json_loads                 | 28.5 us                                                | 29.0 us: 1.02x slower                                                    |
| pyflate                    | 482 ms                                                 | 491 ms: 1.02x slower                                                     |
| bench_thread_pool          | 842 us                                                 | 859 us: 1.02x slower                                                     |
| 2to3                       | 274 ms                                                 | 282 ms: 1.03x slower                                                     |
| richards_super             | 51.5 ms                                                | 53.0 ms: 1.03x slower                                                    |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                     |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                    |
| unpickle_pure_python       | 230 us                                                 | 238 us: 1.03x slower                                                     |
| regex_effbot               | 3.61 ms                                                | 3.75 ms: 1.04x slower                                                    |
| sympy_integrate            | 21.4 ms                                                | 22.3 ms: 1.04x slower                                                    |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                   |
| dulwich_log                | 68.5 ms                                                | 71.4 ms: 1.04x slower                                                    |
| regex_dna                  | 212 ms                                                 | 221 ms: 1.04x slower                                                     |
| sympy_expand               | 478 ms                                                 | 501 ms: 1.05x slower                                                     |
| gc_traversal               | 3.79 ms                                                | 3.99 ms: 1.05x slower                                                    |
| json                       | 5.26 ms                                                | 5.54 ms: 1.05x slower                                                    |
| asyncio_tcp                | 491 ms                                                 | 518 ms: 1.05x slower                                                     |
| sqlglot_optimize           | 54.8 ms                                                | 58.0 ms: 1.06x slower                                                    |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                    |
| gunicorn                   | 1.24 ms                                                | 1.32 ms: 1.06x slower                                                    |
| docutils                   | 2.77 sec                                               | 2.94 sec: 1.06x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 24.7 ms: 1.07x slower                                                    |
| scimark_sor                | 129 ms                                                 | 138 ms: 1.07x slower                                                     |
| mdp                        | 2.63 sec                                               | 2.82 sec: 1.07x slower                                                   |
| django_template            | 34.6 ms                                                | 37.1 ms: 1.07x slower                                                    |
| scimark_lu                 | 118 ms                                                 | 130 ms: 1.10x slower                                                     |
| nqueens                    | 83.3 ms                                                | 93.5 ms: 1.12x slower                                                    |
| go                         | 139 ms                                                 | 158 ms: 1.13x slower                                                     |
| create_gc_cycles           | 1.48 ms                                                | 1.68 ms: 1.14x slower                                                    |
| hexiom                     | 6.41 ms                                                | 7.33 ms: 1.14x slower                                                    |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                    |
| telco                      | 7.10 ms                                                | 8.71 ms: 1.23x slower                                                    |
| coverage                   | 72.7 ms                                                | 95.8 ms: 1.32x slower                                                    |
| python_startup_no_site     | 6.94 ms                                                | 9.51 ms: 1.37x slower                                                    |
| unpack_sequence            | 54.0 ns                                                | 85.6 ns: 1.59x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (7): mypy2, pprint_safe_repr, pprint_pformat, bench_mp_pool, xml_etree_parse, xml_etree_iterparse, pycparser
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 63.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.05x
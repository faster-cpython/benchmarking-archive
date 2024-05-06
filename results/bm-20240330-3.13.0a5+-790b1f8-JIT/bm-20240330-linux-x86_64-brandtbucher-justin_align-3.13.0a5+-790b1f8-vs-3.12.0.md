# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.00x slower
- HPT reliability: 81.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 281 ms: 1.02x slower                                                 |
| chameleon      | 7.41 ms                                                | 7.22 ms: 1.03x faster                                                |
| docutils       | 2.77 sec                                               | 2.91 sec: 1.05x slower                                               |
| tornado_http   | 103 ms                                                 | 97.5 ms: 1.05x faster                                                |
| Geometric mean | (ref)                                                  | 1.00x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 345 ms: 1.30x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 922 ms: 1.28x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 454 ms: 1.27x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 585 ms: 1.24x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 952 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 603 ms: 1.20x faster                                                 |
| async_tree_none            | 472 ms                                                 | 394 ms: 1.20x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.4 ms: 1.08x faster                                                |
| nbody          | 97.0 ms                                                | 93.6 ms: 1.04x faster                                                |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 153 ms: 1.03x slower                                                 |
| regex_effbot   | 3.61 ms                                                | 3.82 ms: 1.06x slower                                                |
| regex_dna      | 212 ms                                                 | 224 ms: 1.06x slower                                                 |
| regex_v8       | 23.1 ms                                                | 25.1 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.18 sec: 1.07x faster                                               |
| pickle_pure_python   | 324 us                                                 | 306 us: 1.06x faster                                                 |
| unpickle             | 15.9 us                                                | 15.2 us: 1.05x faster                                                |
| pickle_dict          | 35.5 us                                                | 34.1 us: 1.04x faster                                                |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.02x faster                                                |
| xml_etree_process    | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                |
| unpickle_list        | 5.29 us                                                | 5.21 us: 1.02x faster                                                |
| xml_etree_generate   | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                |
| json_loads           | 28.5 us                                                | 28.7 us: 1.01x slower                                                |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                 |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                |
| unpickle_pure_python | 230 us                                                 | 251 us: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                |
| python_startup_no_site | 6.94 ms                                                | 9.51 ms: 1.37x slower                                                |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.4 ms: 1.05x faster                                                |
| django_template | 34.6 ms                                                | 36.1 ms: 1.04x slower                                                |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.39x faster                                                 |
| async_tree_none_tg         | 450 ms                                                 | 345 ms: 1.30x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 922 ms: 1.28x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 454 ms: 1.27x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 585 ms: 1.24x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 952 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 603 ms: 1.20x faster                                                 |
| async_tree_none            | 472 ms                                                 | 394 ms: 1.20x faster                                                 |
| comprehensions             | 21.8 us                                                | 19.3 us: 1.13x faster                                                |
| logging_format             | 7.23 us                                                | 6.55 us: 1.10x faster                                                |
| logging_simple             | 6.46 us                                                | 5.98 us: 1.08x faster                                                |
| float                      | 84.7 ms                                                | 78.4 ms: 1.08x faster                                                |
| tomli_loads                | 2.33 sec                                               | 2.18 sec: 1.07x faster                                               |
| scimark_fft                | 382 ms                                                 | 357 ms: 1.07x faster                                                 |
| crypto_pyaes               | 81.9 ms                                                | 77.1 ms: 1.06x faster                                                |
| deltablue                  | 3.72 ms                                                | 3.50 ms: 1.06x faster                                                |
| pickle_pure_python         | 324 us                                                 | 306 us: 1.06x faster                                                 |
| raytrace                   | 312 ms                                                 | 296 ms: 1.05x faster                                                 |
| tornado_http               | 103 ms                                                 | 97.5 ms: 1.05x faster                                                |
| logging_silent             | 104 ns                                                 | 99.6 ns: 1.05x faster                                                |
| mako                       | 11.9 ms                                                | 11.4 ms: 1.05x faster                                                |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.05x faster                                                |
| pickle_dict                | 35.5 us                                                | 34.1 us: 1.04x faster                                                |
| chaos                      | 67.0 ms                                                | 64.4 ms: 1.04x faster                                                |
| nbody                      | 97.0 ms                                                | 93.6 ms: 1.04x faster                                                |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                                |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                |
| chameleon                  | 7.41 ms                                                | 7.22 ms: 1.03x faster                                                |
| scimark_monte_carlo        | 75.1 ms                                                | 73.3 ms: 1.03x faster                                                |
| pickle_list                | 5.08 us                                                | 4.96 us: 1.02x faster                                                |
| gc_traversal               | 3.79 ms                                                | 3.71 ms: 1.02x faster                                                |
| deepcopy                   | 371 us                                                 | 364 us: 1.02x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.02x faster                                                |
| sympy_str                  | 300 ms                                                 | 294 ms: 1.02x faster                                                 |
| deepcopy_memo              | 40.7 us                                                | 40.0 us: 1.02x faster                                                |
| xml_etree_process          | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                |
| sqlglot_transpile          | 1.68 ms                                                | 1.66 ms: 1.02x faster                                                |
| unpickle_list              | 5.29 us                                                | 5.21 us: 1.02x faster                                                |
| fannkuch                   | 417 ms                                                 | 411 ms: 1.02x faster                                                 |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                 |
| xml_etree_generate         | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                |
| pathlib                    | 19.3 ms                                                | 19.2 ms: 1.01x faster                                                |
| meteor_contest             | 112 ms                                                 | 112 ms: 1.00x faster                                                 |
| sqlite_synth               | 2.83 us                                                | 2.85 us: 1.01x slower                                                |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.09 ms: 1.01x slower                                                |
| json_loads                 | 28.5 us                                                | 28.7 us: 1.01x slower                                                |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                 |
| mdp                        | 2.63 sec                                               | 2.66 sec: 1.01x slower                                               |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                 |
| dask                       | 372 ms                                                 | 377 ms: 1.01x slower                                                 |
| bench_thread_pool          | 842 us                                                 | 857 us: 1.02x slower                                                 |
| json                       | 5.26 ms                                                | 5.36 ms: 1.02x slower                                                |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                |
| 2to3                       | 274 ms                                                 | 281 ms: 1.02x slower                                                 |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                                |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.03x slower                                                 |
| pprint_safe_repr           | 776 ms                                                 | 798 ms: 1.03x slower                                                 |
| pprint_pformat             | 1.57 sec                                               | 1.61 sec: 1.03x slower                                               |
| regex_compile              | 148 ms                                                 | 153 ms: 1.03x slower                                                 |
| asyncio_websockets         | 551 ms                                                 | 570 ms: 1.03x slower                                                 |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.04x slower                                               |
| asyncio_tcp                | 491 ms                                                 | 510 ms: 1.04x slower                                                 |
| dulwich_log                | 68.5 ms                                                | 71.4 ms: 1.04x slower                                                |
| sympy_expand               | 478 ms                                                 | 499 ms: 1.04x slower                                                 |
| django_template            | 34.6 ms                                                | 36.1 ms: 1.04x slower                                                |
| pyflate                    | 482 ms                                                 | 505 ms: 1.05x slower                                                 |
| docutils                   | 2.77 sec                                               | 2.91 sec: 1.05x slower                                               |
| spectral_norm              | 115 ms                                                 | 121 ms: 1.05x slower                                                 |
| sqlglot_optimize           | 54.8 ms                                                | 57.8 ms: 1.05x slower                                                |
| regex_effbot               | 3.61 ms                                                | 3.82 ms: 1.06x slower                                                |
| regex_dna                  | 212 ms                                                 | 224 ms: 1.06x slower                                                 |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                |
| richards_super             | 51.5 ms                                                | 54.6 ms: 1.06x slower                                                |
| richards                   | 45.8 ms                                                | 48.7 ms: 1.06x slower                                                |
| gunicorn                   | 1.24 ms                                                | 1.32 ms: 1.06x slower                                                |
| regex_v8                   | 23.1 ms                                                | 25.1 ms: 1.09x slower                                                |
| unpickle_pure_python       | 230 us                                                 | 251 us: 1.09x slower                                                 |
| nqueens                    | 83.3 ms                                                | 93.4 ms: 1.12x slower                                                |
| create_gc_cycles           | 1.48 ms                                                | 1.66 ms: 1.13x slower                                                |
| scimark_lu                 | 118 ms                                                 | 134 ms: 1.14x slower                                                 |
| go                         | 139 ms                                                 | 159 ms: 1.14x slower                                                 |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                |
| hexiom                     | 6.41 ms                                                | 7.56 ms: 1.18x slower                                                |
| telco                      | 7.10 ms                                                | 8.68 ms: 1.22x slower                                                |
| coverage                   | 72.7 ms                                                | 97.8 ms: 1.35x slower                                                |
| python_startup_no_site     | 6.94 ms                                                | 9.51 ms: 1.37x slower                                                |
| unpack_sequence            | 54.0 ns                                                | 125 ns: 2.31x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (5): mypy2, async_generators, bench_mp_pool, xml_etree_parse, pycparser
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 81.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.04x
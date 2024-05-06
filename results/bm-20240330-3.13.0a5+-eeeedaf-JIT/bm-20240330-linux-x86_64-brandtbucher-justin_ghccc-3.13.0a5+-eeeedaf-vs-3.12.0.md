# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.02x faster
- HPT reliability: 90.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 276 ms: 1.01x slower                                                 |
| chameleon      | 7.41 ms                                                | 7.05 ms: 1.05x faster                                                |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                               |
| tornado_http   | 103 ms                                                 | 97.0 ms: 1.06x faster                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 907 ms: 1.30x faster                                                 |
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.30x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 447 ms: 1.28x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 450 ms: 1.28x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 929 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 599 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 72.8 ms: 1.16x faster                                                |
| nbody          | 97.0 ms                                                | 87.0 ms: 1.11x faster                                                |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 143 ms: 1.04x faster                                                 |
| regex_effbot   | 3.61 ms                                                | 3.63 ms: 1.00x slower                                                |
| regex_dna      | 212 ms                                                 | 219 ms: 1.03x slower                                                 |
| regex_v8       | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.02 sec: 1.16x faster                                               |
| pickle_pure_python   | 324 us                                                 | 308 us: 1.05x faster                                                 |
| unpickle             | 15.9 us                                                | 15.2 us: 1.05x faster                                                |
| pickle_dict          | 35.5 us                                                | 34.2 us: 1.04x faster                                                |
| xml_etree_process    | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                |
| pickle_list          | 5.08 us                                                | 4.97 us: 1.02x faster                                                |
| unpickle_list        | 5.29 us                                                | 5.23 us: 1.01x faster                                                |
| unpickle_pure_python | 230 us                                                 | 229 us: 1.01x faster                                                 |
| xml_etree_iterparse  | 107 ms                                                 | 106 ms: 1.01x faster                                                 |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.16x slower                                                |
| python_startup_no_site | 6.94 ms                                                | 9.49 ms: 1.37x slower                                                |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 9.96 ms: 1.19x faster                                                |
| django_template | 34.6 ms                                                | 36.4 ms: 1.05x slower                                                |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.39x faster                                                 |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 907 ms: 1.30x faster                                                 |
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.30x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 447 ms: 1.28x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 450 ms: 1.28x faster                                                 |
| comprehensions             | 21.8 us                                                | 17.4 us: 1.25x faster                                                |
| async_tree_io              | 1.16 sec                                               | 929 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 599 ms: 1.21x faster                                                 |
| scimark_fft                | 382 ms                                                 | 319 ms: 1.20x faster                                                 |
| mako                       | 11.9 ms                                                | 9.96 ms: 1.19x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                 |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.33 ms: 1.17x faster                                                |
| crypto_pyaes               | 81.9 ms                                                | 70.1 ms: 1.17x faster                                                |
| float                      | 84.7 ms                                                | 72.8 ms: 1.16x faster                                                |
| scimark_monte_carlo        | 75.1 ms                                                | 64.9 ms: 1.16x faster                                                |
| tomli_loads                | 2.33 sec                                               | 2.02 sec: 1.16x faster                                               |
| spectral_norm              | 115 ms                                                 | 101 ms: 1.14x faster                                                 |
| fannkuch                   | 417 ms                                                 | 367 ms: 1.14x faster                                                 |
| raytrace                   | 312 ms                                                 | 279 ms: 1.12x faster                                                 |
| nbody                      | 97.0 ms                                                | 87.0 ms: 1.11x faster                                                |
| chaos                      | 67.0 ms                                                | 60.3 ms: 1.11x faster                                                |
| logging_format             | 7.23 us                                                | 6.57 us: 1.10x faster                                                |
| logging_simple             | 6.46 us                                                | 5.94 us: 1.09x faster                                                |
| pyflate                    | 482 ms                                                 | 451 ms: 1.07x faster                                                 |
| deltablue                  | 3.72 ms                                                | 3.48 ms: 1.07x faster                                                |
| tornado_http               | 103 ms                                                 | 97.0 ms: 1.06x faster                                                |
| pickle_pure_python         | 324 us                                                 | 308 us: 1.05x faster                                                 |
| pprint_safe_repr           | 776 ms                                                 | 738 ms: 1.05x faster                                                 |
| chameleon                  | 7.41 ms                                                | 7.05 ms: 1.05x faster                                                |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.05x faster                                                |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                                |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                               |
| pickle_dict                | 35.5 us                                                | 34.2 us: 1.04x faster                                                |
| regex_compile              | 148 ms                                                 | 143 ms: 1.04x faster                                                 |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                |
| coroutines                 | 23.2 ms                                                | 22.4 ms: 1.03x faster                                                |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                 |
| sympy_sum                  | 169 ms                                                 | 164 ms: 1.03x faster                                                 |
| sympy_str                  | 300 ms                                                 | 291 ms: 1.03x faster                                                 |
| gc_traversal               | 3.79 ms                                                | 3.69 ms: 1.03x faster                                                |
| xml_etree_process          | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.03x faster                                                |
| pickle_list                | 5.08 us                                                | 4.97 us: 1.02x faster                                                |
| deepcopy                   | 371 us                                                 | 363 us: 1.02x faster                                                 |
| sqlglot_transpile          | 1.68 ms                                                | 1.65 ms: 1.02x faster                                                |
| deepcopy_memo              | 40.7 us                                                | 40.1 us: 1.02x faster                                                |
| pathlib                    | 19.3 ms                                                | 19.1 ms: 1.01x faster                                                |
| unpickle_list              | 5.29 us                                                | 5.23 us: 1.01x faster                                                |
| logging_silent             | 104 ns                                                 | 104 ns: 1.01x faster                                                 |
| unpickle_pure_python       | 230 us                                                 | 229 us: 1.01x faster                                                 |
| xml_etree_iterparse        | 107 ms                                                 | 106 ms: 1.01x faster                                                 |
| regex_effbot               | 3.61 ms                                                | 3.63 ms: 1.00x slower                                                |
| 2to3                       | 274 ms                                                 | 276 ms: 1.01x slower                                                 |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                 |
| async_generators           | 463 ms                                                 | 468 ms: 1.01x slower                                                 |
| pycparser                  | 1.18 sec                                               | 1.19 sec: 1.01x slower                                               |
| sympy_integrate            | 21.4 ms                                                | 21.7 ms: 1.02x slower                                                |
| bench_thread_pool          | 842 us                                                 | 858 us: 1.02x slower                                                 |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                |
| asyncio_websockets         | 551 ms                                                 | 570 ms: 1.03x slower                                                 |
| regex_dna                  | 212 ms                                                 | 219 ms: 1.03x slower                                                 |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.04x slower                                               |
| sympy_expand               | 478 ms                                                 | 497 ms: 1.04x slower                                                 |
| asyncio_tcp                | 491 ms                                                 | 510 ms: 1.04x slower                                                 |
| dulwich_log                | 68.5 ms                                                | 71.6 ms: 1.04x slower                                                |
| json                       | 5.26 ms                                                | 5.50 ms: 1.04x slower                                                |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                               |
| sqlglot_normalize          | 110 ms                                                 | 115 ms: 1.05x slower                                                 |
| django_template            | 34.6 ms                                                | 36.4 ms: 1.05x slower                                                |
| scimark_sor                | 129 ms                                                 | 136 ms: 1.05x slower                                                 |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                |
| gunicorn                   | 1.24 ms                                                | 1.32 ms: 1.06x slower                                                |
| sqlglot_optimize           | 54.8 ms                                                | 58.7 ms: 1.07x slower                                                |
| hexiom                     | 6.41 ms                                                | 6.88 ms: 1.07x slower                                                |
| regex_v8                   | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                |
| nqueens                    | 83.3 ms                                                | 91.2 ms: 1.10x slower                                                |
| scimark_lu                 | 118 ms                                                 | 130 ms: 1.10x slower                                                 |
| create_gc_cycles           | 1.48 ms                                                | 1.66 ms: 1.13x slower                                                |
| go                         | 139 ms                                                 | 158 ms: 1.13x slower                                                 |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.16x slower                                                |
| telco                      | 7.10 ms                                                | 8.55 ms: 1.20x slower                                                |
| coverage                   | 72.7 ms                                                | 96.9 ms: 1.33x slower                                                |
| python_startup_no_site     | 6.94 ms                                                | 9.49 ms: 1.37x slower                                                |
| unpack_sequence            | 54.0 ns                                                | 115 ns: 2.12x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (9): mypy2, bench_mp_pool, mdp, richards, sqlite_synth, richards_super, xml_etree_parse, json_loads, dask
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 90.15% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x
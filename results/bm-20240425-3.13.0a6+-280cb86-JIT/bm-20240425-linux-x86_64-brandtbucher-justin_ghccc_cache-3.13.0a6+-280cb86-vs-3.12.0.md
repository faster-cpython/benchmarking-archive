# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 280cb86
- commit date: 2024-04-25
- overall geometric mean: 1.05x faster
- HPT reliability: 98.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 275 ms: 1.00x slower                                                       |
| chameleon      | 7.41 ms                                                | 6.94 ms: 1.07x faster                                                      |
| docutils       | 2.77 sec                                               | 2.92 sec: 1.05x slower                                                     |
| tornado_http   | 103 ms                                                 | 95.3 ms: 1.08x faster                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                       |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                       |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                       |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                       |
| async_tree_io_tg           | 1.18 sec                                               | 947 ms: 1.25x faster                                                       |
| async_tree_io              | 1.16 sec                                               | 937 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                       |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 75.3 ms: 1.29x faster                                                      |
| float          | 84.7 ms                                                | 72.6 ms: 1.17x faster                                                      |
| pidigits       | 187 ms                                                 | 193 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                  | 1.13x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 140 ms: 1.06x faster                                                       |
| regex_effbot   | 3.61 ms                                                | 3.76 ms: 1.04x slower                                                      |
| regex_dna      | 212 ms                                                 | 230 ms: 1.08x slower                                                       |
| regex_v8       | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.90 sec: 1.23x faster                                                     |
| xml_etree_parse      | 159 ms                                                 | 148 ms: 1.08x faster                                                       |
| pickle_pure_python   | 324 us                                                 | 306 us: 1.06x faster                                                       |
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                      |
| xml_etree_iterparse  | 107 ms                                                 | 102 ms: 1.05x faster                                                       |
| xml_etree_process    | 61.7 ms                                                | 59.7 ms: 1.03x faster                                                      |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                      |
| unpickle_pure_python | 230 us                                                 | 223 us: 1.03x faster                                                       |
| unpickle_list        | 5.29 us                                                | 5.14 us: 1.03x faster                                                      |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                      |
| pickle_dict          | 35.5 us                                                | 34.6 us: 1.03x faster                                                      |
| pickle               | 11.6 us                                                | 11.5 us: 1.01x faster                                                      |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                               |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.71 ms: 1.11x slower                                                      |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.0 ms: 1.19x faster                                                      |
| django_template | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 116 us: 1.36x faster                                                       |
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                       |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                       |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                       |
| nbody                      | 97.0 ms                                                | 75.3 ms: 1.29x faster                                                      |
| comprehensions             | 21.8 us                                                | 17.1 us: 1.27x faster                                                      |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                       |
| async_tree_io_tg           | 1.18 sec                                               | 947 ms: 1.25x faster                                                       |
| scimark_fft                | 382 ms                                                 | 308 ms: 1.24x faster                                                       |
| async_tree_io              | 1.16 sec                                               | 937 ms: 1.23x faster                                                       |
| tomli_loads                | 2.33 sec                                               | 1.90 sec: 1.23x faster                                                     |
| scimark_monte_carlo        | 75.1 ms                                                | 61.9 ms: 1.21x faster                                                      |
| crypto_pyaes               | 81.9 ms                                                | 67.7 ms: 1.21x faster                                                      |
| fannkuch                   | 417 ms                                                 | 345 ms: 1.21x faster                                                       |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                       |
| mako                       | 11.9 ms                                                | 10.0 ms: 1.19x faster                                                      |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                       |
| float                      | 84.7 ms                                                | 72.6 ms: 1.17x faster                                                      |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.38 ms: 1.15x faster                                                      |
| spectral_norm              | 115 ms                                                 | 99.7 ms: 1.15x faster                                                      |
| raytrace                   | 312 ms                                                 | 271 ms: 1.15x faster                                                       |
| chaos                      | 67.0 ms                                                | 59.3 ms: 1.13x faster                                                      |
| pyflate                    | 482 ms                                                 | 432 ms: 1.12x faster                                                       |
| logging_format             | 7.23 us                                                | 6.50 us: 1.11x faster                                                      |
| logging_simple             | 6.46 us                                                | 5.82 us: 1.11x faster                                                      |
| richards                   | 45.8 ms                                                | 41.9 ms: 1.09x faster                                                      |
| tornado_http               | 103 ms                                                 | 95.3 ms: 1.08x faster                                                      |
| xml_etree_parse            | 159 ms                                                 | 148 ms: 1.08x faster                                                       |
| richards_super             | 51.5 ms                                                | 48.0 ms: 1.07x faster                                                      |
| pprint_safe_repr           | 776 ms                                                 | 724 ms: 1.07x faster                                                       |
| pathlib                    | 19.3 ms                                                | 18.1 ms: 1.07x faster                                                      |
| chameleon                  | 7.41 ms                                                | 6.94 ms: 1.07x faster                                                      |
| mypy2                      | 830 ms                                                 | 779 ms: 1.07x faster                                                       |
| regex_compile              | 148 ms                                                 | 140 ms: 1.06x faster                                                       |
| pprint_pformat             | 1.57 sec                                               | 1.48 sec: 1.06x faster                                                     |
| pickle_pure_python         | 324 us                                                 | 306 us: 1.06x faster                                                       |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                 | 102 ms: 1.05x faster                                                       |
| generators                 | 31.2 ms                                                | 29.9 ms: 1.04x faster                                                      |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                      |
| deepcopy_memo              | 40.7 us                                                | 39.2 us: 1.04x faster                                                      |
| xml_etree_process          | 61.7 ms                                                | 59.7 ms: 1.03x faster                                                      |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                                      |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                      |
| unpickle_pure_python       | 230 us                                                 | 223 us: 1.03x faster                                                       |
| unpickle_list              | 5.29 us                                                | 5.14 us: 1.03x faster                                                      |
| sympy_str                  | 300 ms                                                 | 291 ms: 1.03x faster                                                       |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                      |
| pickle_dict                | 35.5 us                                                | 34.6 us: 1.03x faster                                                      |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                       |
| logging_silent             | 104 ns                                                 | 102 ns: 1.02x faster                                                       |
| deltablue                  | 3.72 ms                                                | 3.63 ms: 1.02x faster                                                      |
| deepcopy                   | 371 us                                                 | 363 us: 1.02x faster                                                       |
| json                       | 5.26 ms                                                | 5.15 ms: 1.02x faster                                                      |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                       |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.01x faster                                                      |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.01x faster                                                     |
| scimark_sor                | 129 ms                                                 | 128 ms: 1.01x faster                                                       |
| pickle                     | 11.6 us                                                | 11.5 us: 1.01x faster                                                      |
| sqlite_synth               | 2.83 us                                                | 2.82 us: 1.01x faster                                                      |
| hexiom                     | 6.41 ms                                                | 6.40 ms: 1.00x faster                                                      |
| 2to3                       | 274 ms                                                 | 275 ms: 1.00x slower                                                       |
| dulwich_log                | 68.5 ms                                                | 68.8 ms: 1.00x slower                                                      |
| async_generators           | 463 ms                                                 | 466 ms: 1.01x slower                                                       |
| sympy_integrate            | 21.4 ms                                                | 21.8 ms: 1.02x slower                                                      |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.02x slower                                                       |
| bench_thread_pool          | 842 us                                                 | 860 us: 1.02x slower                                                       |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                      |
| mdp                        | 2.63 sec                                               | 2.69 sec: 1.02x slower                                                     |
| asyncio_websockets         | 551 ms                                                 | 565 ms: 1.02x slower                                                       |
| pidigits                   | 187 ms                                                 | 193 ms: 1.03x slower                                                       |
| nqueens                    | 83.3 ms                                                | 86.0 ms: 1.03x slower                                                      |
| sympy_expand               | 478 ms                                                 | 494 ms: 1.03x slower                                                       |
| sqlglot_optimize           | 54.8 ms                                                | 56.7 ms: 1.04x slower                                                      |
| django_template            | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                      |
| regex_effbot               | 3.61 ms                                                | 3.76 ms: 1.04x slower                                                      |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                     |
| gunicorn                   | 1.24 ms                                                | 1.29 ms: 1.04x slower                                                      |
| asyncio_tcp                | 491 ms                                                 | 516 ms: 1.05x slower                                                       |
| go                         | 139 ms                                                 | 147 ms: 1.05x slower                                                       |
| docutils                   | 2.77 sec                                               | 2.92 sec: 1.05x slower                                                     |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                      |
| scimark_lu                 | 118 ms                                                 | 125 ms: 1.06x slower                                                       |
| gc_traversal               | 3.79 ms                                                | 4.06 ms: 1.07x slower                                                      |
| regex_dna                  | 212 ms                                                 | 230 ms: 1.08x slower                                                       |
| regex_v8                   | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                      |
| python_startup_no_site     | 6.94 ms                                                | 7.71 ms: 1.11x slower                                                      |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                      |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                      |
| telco                      | 7.10 ms                                                | 8.57 ms: 1.21x slower                                                      |
| coverage                   | 72.7 ms                                                | 97.2 ms: 1.34x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                               |

Benchmark hidden because not significant (3): bench_mp_pool, pickle_list, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240425-3.13.0a6+-280cb86-JIT/bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.80% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x
# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_perf
- machine: linux-x86_64
- commit hash: f7a4afd
- commit date: 2024-04-23
- overall geometric mean: 1.04x faster
- HPT reliability: 98.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 275 ms: 1.00x slower                                                      |
| chameleon      | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                     |
| docutils       | 2.77 sec                                               | 2.91 sec: 1.05x slower                                                    |
| tornado_http   | 103 ms                                                 | 95.7 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                  | 1.02x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 340 ms: 1.32x faster                                                      |
| async_tree_none            | 472 ms                                                 | 360 ms: 1.31x faster                                                      |
| async_tree_memoization_tg  | 575 ms                                                 | 447 ms: 1.28x faster                                                      |
| async_tree_memoization     | 578 ms                                                 | 458 ms: 1.26x faster                                                      |
| async_tree_io_tg           | 1.18 sec                                               | 949 ms: 1.25x faster                                                      |
| async_tree_io              | 1.16 sec                                               | 932 ms: 1.24x faster                                                      |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.19x faster                                                      |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 618 ms: 1.17x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 82.4 ms: 1.18x faster                                                     |
| float          | 84.7 ms                                                | 74.9 ms: 1.13x faster                                                     |
| pidigits       | 187 ms                                                 | 192 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                  | 1.09x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 140 ms: 1.06x faster                                                      |
| regex_effbot   | 3.61 ms                                                | 3.80 ms: 1.05x slower                                                     |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                      |
| regex_v8       | 23.1 ms                                                | 24.6 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                  | 1.03x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.96 sec: 1.19x faster                                                    |
| xml_etree_parse      | 159 ms                                                 | 150 ms: 1.06x faster                                                      |
| pickle_pure_python   | 324 us                                                 | 307 us: 1.06x faster                                                      |
| unpickle             | 15.9 us                                                | 15.2 us: 1.04x faster                                                     |
| xml_etree_iterparse  | 107 ms                                                 | 103 ms: 1.04x faster                                                      |
| pickle_dict          | 35.5 us                                                | 34.4 us: 1.03x faster                                                     |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                     |
| xml_etree_process    | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                     |
| unpickle_list        | 5.29 us                                                | 5.18 us: 1.02x faster                                                     |
| unpickle_pure_python | 230 us                                                 | 227 us: 1.01x faster                                                      |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                     |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                     |
| pickle_list          | 5.08 us                                                | 5.17 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.60 ms: 1.10x slower                                                     |
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.1 ms: 1.18x faster                                                     |
| django_template | 34.6 ms                                                | 36.7 ms: 1.06x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.06x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 112 us: 1.41x faster                                                      |
| async_tree_none_tg         | 450 ms                                                 | 340 ms: 1.32x faster                                                      |
| async_tree_none            | 472 ms                                                 | 360 ms: 1.31x faster                                                      |
| async_tree_memoization_tg  | 575 ms                                                 | 447 ms: 1.28x faster                                                      |
| comprehensions             | 21.8 us                                                | 17.1 us: 1.27x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 458 ms: 1.26x faster                                                      |
| async_tree_io_tg           | 1.18 sec                                               | 949 ms: 1.25x faster                                                      |
| async_tree_io              | 1.16 sec                                               | 932 ms: 1.24x faster                                                      |
| scimark_fft                | 382 ms                                                 | 315 ms: 1.21x faster                                                      |
| tomli_loads                | 2.33 sec                                               | 1.96 sec: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.19x faster                                                      |
| mako                       | 11.9 ms                                                | 10.1 ms: 1.18x faster                                                     |
| nbody                      | 97.0 ms                                                | 82.4 ms: 1.18x faster                                                     |
| crypto_pyaes               | 81.9 ms                                                | 69.6 ms: 1.18x faster                                                     |
| spectral_norm              | 115 ms                                                 | 97.8 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 618 ms: 1.17x faster                                                      |
| scimark_monte_carlo        | 75.1 ms                                                | 64.2 ms: 1.17x faster                                                     |
| raytrace                   | 312 ms                                                 | 272 ms: 1.15x faster                                                      |
| fannkuch                   | 417 ms                                                 | 364 ms: 1.15x faster                                                      |
| float                      | 84.7 ms                                                | 74.9 ms: 1.13x faster                                                     |
| chaos                      | 67.0 ms                                                | 60.7 ms: 1.10x faster                                                     |
| logging_format             | 7.23 us                                                | 6.56 us: 1.10x faster                                                     |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.62 ms: 1.09x faster                                                     |
| pyflate                    | 482 ms                                                 | 444 ms: 1.09x faster                                                      |
| logging_simple             | 6.46 us                                                | 5.94 us: 1.09x faster                                                     |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.09x faster                                                     |
| richards                   | 45.8 ms                                                | 42.3 ms: 1.08x faster                                                     |
| tornado_http               | 103 ms                                                 | 95.7 ms: 1.07x faster                                                     |
| xml_etree_parse            | 159 ms                                                 | 150 ms: 1.06x faster                                                      |
| regex_compile              | 148 ms                                                 | 140 ms: 1.06x faster                                                      |
| chameleon                  | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                     |
| pickle_pure_python         | 324 us                                                 | 307 us: 1.06x faster                                                      |
| richards_super             | 51.5 ms                                                | 48.9 ms: 1.05x faster                                                     |
| deepcopy_memo              | 40.7 us                                                | 38.8 us: 1.05x faster                                                     |
| pprint_safe_repr           | 776 ms                                                 | 741 ms: 1.05x faster                                                      |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                                     |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.04x faster                                                     |
| coroutines                 | 23.2 ms                                                | 22.2 ms: 1.04x faster                                                     |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                                    |
| xml_etree_iterparse        | 107 ms                                                 | 103 ms: 1.04x faster                                                      |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                     |
| pickle_dict                | 35.5 us                                                | 34.4 us: 1.03x faster                                                     |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                      |
| deepcopy                   | 371 us                                                 | 360 us: 1.03x faster                                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                     |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                     |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                      |
| xml_etree_process          | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                     |
| sqlglot_transpile          | 1.68 ms                                                | 1.64 ms: 1.03x faster                                                     |
| sympy_str                  | 300 ms                                                 | 293 ms: 1.02x faster                                                      |
| json                       | 5.26 ms                                                | 5.15 ms: 1.02x faster                                                     |
| unpickle_list              | 5.29 us                                                | 5.18 us: 1.02x faster                                                     |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                      |
| unpickle_pure_python       | 230 us                                                 | 227 us: 1.01x faster                                                      |
| pycparser                  | 1.18 sec                                               | 1.17 sec: 1.01x faster                                                    |
| scimark_sor                | 129 ms                                                 | 128 ms: 1.01x faster                                                      |
| gc_traversal               | 3.79 ms                                                | 3.80 ms: 1.00x slower                                                     |
| 2to3                       | 274 ms                                                 | 275 ms: 1.00x slower                                                      |
| async_generators           | 463 ms                                                 | 465 ms: 1.00x slower                                                      |
| dulwich_log                | 68.5 ms                                                | 68.9 ms: 1.01x slower                                                     |
| sqlite_synth               | 2.83 us                                                | 2.86 us: 1.01x slower                                                     |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                     |
| bench_thread_pool          | 842 us                                                 | 853 us: 1.01x slower                                                      |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                     |
| pickle_list                | 5.08 us                                                | 5.17 us: 1.02x slower                                                     |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                                     |
| hexiom                     | 6.41 ms                                                | 6.58 ms: 1.03x slower                                                     |
| pidigits                   | 187 ms                                                 | 192 ms: 1.03x slower                                                      |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                                      |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.03x slower                                                      |
| sympy_expand               | 478 ms                                                 | 496 ms: 1.04x slower                                                      |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                    |
| sqlglot_optimize           | 54.8 ms                                                | 57.3 ms: 1.04x slower                                                     |
| asyncio_tcp                | 491 ms                                                 | 513 ms: 1.04x slower                                                      |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                     |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                     |
| docutils                   | 2.77 sec                                               | 2.91 sec: 1.05x slower                                                    |
| regex_effbot               | 3.61 ms                                                | 3.80 ms: 1.05x slower                                                     |
| nqueens                    | 83.3 ms                                                | 87.9 ms: 1.05x slower                                                     |
| django_template            | 34.6 ms                                                | 36.7 ms: 1.06x slower                                                     |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                      |
| regex_v8                   | 23.1 ms                                                | 24.6 ms: 1.06x slower                                                     |
| mdp                        | 2.63 sec                                               | 2.84 sec: 1.08x slower                                                    |
| scimark_lu                 | 118 ms                                                 | 128 ms: 1.09x slower                                                      |
| python_startup_no_site     | 6.94 ms                                                | 7.60 ms: 1.10x slower                                                     |
| go                         | 139 ms                                                 | 154 ms: 1.11x slower                                                      |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                     |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                                     |
| telco                      | 7.10 ms                                                | 8.67 ms: 1.22x slower                                                     |
| coverage                   | 72.7 ms                                                | 98.6 ms: 1.36x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                              |

Benchmark hidden because not significant (5): mypy2, deltablue, json_loads, bench_mp_pool, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-f7a4afd-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.27% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_recompile
- machine: linux-x86_64
- commit hash: 0cc257c
- commit date: 2024-05-08
- overall geometric mean: 1.02x slower
- HPT reliability: 65.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.14x slower                                                    |
| chameleon      | 6.70 ms                                                | 7.11 ms: 1.06x slower                                                   |
| docutils       | 2.66 sec                                               | 3.83 sec: 1.44x slower                                                  |
| html5lib       | 64.8 ms                                                | 75.0 ms: 1.16x slower                                                   |
| tornado_http   | 98.1 ms                                                | 99.4 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.29 sec                                               | 1.18 sec: 1.09x faster                                                  |
| async_tree_none            | 528 ms                                                 | 489 ms: 1.08x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 1.21 sec: 1.07x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 588 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 718 ms: 1.06x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 467 ms: 1.05x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 618 ms: 1.03x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.0 ms: 1.19x faster                                                   |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                    |
| float          | 78.9 ms                                                | 89.8 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                    |
| regex_dna      | 205 ms                                                 | 224 ms: 1.10x slower                                                    |
| regex_effbot   | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                   |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 2.02 sec: 1.14x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                                    |
| pickle_pure_python   | 320 us                                                 | 307 us: 1.04x faster                                                    |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.2 us: 1.01x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.26 us: 1.01x slower                                                   |
| xml_etree_parse      | 164 ms                                                 | 174 ms: 1.06x slower                                                    |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                   |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 93.2 ms: 1.15x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 66.2 ms: 1.16x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.46 us: 1.19x slower                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 140 ms: 1.29x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.68 ms: 1.28x slower                                                   |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.72 ms: 1.10x faster                                                   |
| django_template | 33.5 ms                                                | 36.4 ms: 1.09x slower                                                   |
| genshi_text     | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                   |
| genshi_xml      | 53.4 ms                                                | 61.3 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 175 us: 2.96x faster                                                    |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.51x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 515 ms: 1.70x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                   |
| richards_super             | 61.9 ms                                                | 50.5 ms: 1.23x faster                                                   |
| chaos                      | 71.9 ms                                                | 58.8 ms: 1.22x faster                                                   |
| nbody                      | 96.0 ms                                                | 81.0 ms: 1.19x faster                                                   |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.17x faster                                                   |
| pylint                     | 476 ms                                                 | 415 ms: 1.15x faster                                                    |
| tomli_loads                | 2.30 sec                                               | 2.02 sec: 1.14x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 67.6 ms: 1.13x faster                                                   |
| richards                   | 49.8 ms                                                | 44.0 ms: 1.13x faster                                                   |
| fannkuch                   | 405 ms                                                 | 363 ms: 1.12x faster                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.54 ms: 1.11x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 64.1 ms: 1.10x faster                                                   |
| raytrace                   | 309 ms                                                 | 280 ms: 1.10x faster                                                    |
| mako                       | 10.7 ms                                                | 9.72 ms: 1.10x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 1.18 sec: 1.09x faster                                                  |
| scimark_fft                | 345 ms                                                 | 318 ms: 1.09x faster                                                    |
| async_tree_none            | 528 ms                                                 | 489 ms: 1.08x faster                                                    |
| unpickle_pure_python       | 242 us                                                 | 224 us: 1.08x faster                                                    |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 1.21 sec: 1.07x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 588 ms: 1.06x faster                                                    |
| deepcopy_memo              | 40.2 us                                                | 37.7 us: 1.06x faster                                                   |
| spectral_norm              | 108 ms                                                 | 102 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 718 ms: 1.06x faster                                                    |
| logging_format             | 6.81 us                                                | 6.45 us: 1.06x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 467 ms: 1.05x faster                                                    |
| pprint_pformat             | 1.55 sec                                               | 1.48 sec: 1.05x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.58 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 747 ms                                                 | 714 ms: 1.05x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 307 us: 1.04x faster                                                    |
| logging_silent             | 111 ns                                                 | 107 ns: 1.03x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 618 ms: 1.03x faster                                                    |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.03x faster                                                   |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                    |
| sqlglot_parse              | 1.43 ms                                                | 1.40 ms: 1.03x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                   |
| nqueens                    | 87.9 ms                                                | 86.6 ms: 1.01x faster                                                   |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                                   |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.74 ms: 1.01x faster                                                   |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x slower                                                    |
| mdp                        | 2.77 sec                                               | 2.80 sec: 1.01x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.26 us: 1.01x slower                                                   |
| json                       | 5.24 ms                                                | 5.30 ms: 1.01x slower                                                   |
| tornado_http               | 98.1 ms                                                | 99.4 ms: 1.01x slower                                                   |
| go                         | 149 ms                                                 | 151 ms: 1.02x slower                                                    |
| deltablue                  | 3.92 ms                                                | 3.99 ms: 1.02x slower                                                   |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                                    |
| sympy_str                  | 297 ms                                                 | 304 ms: 1.02x slower                                                    |
| pyflate                    | 434 ms                                                 | 444 ms: 1.02x slower                                                    |
| deepcopy                   | 365 us                                                 | 374 us: 1.02x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                    |
| sympy_sum                  | 169 ms                                                 | 173 ms: 1.03x slower                                                    |
| thrift                     | 784 us                                                 | 814 us: 1.04x slower                                                    |
| bench_thread_pool          | 834 us                                                 | 871 us: 1.04x slower                                                    |
| deepcopy_reduce            | 3.22 us                                                | 3.39 us: 1.05x slower                                                   |
| sympy_expand               | 484 ms                                                 | 513 ms: 1.06x slower                                                    |
| chameleon                  | 6.70 ms                                                | 7.11 ms: 1.06x slower                                                   |
| sympy_integrate            | 21.5 ms                                                | 22.8 ms: 1.06x slower                                                   |
| xml_etree_parse            | 164 ms                                                 | 174 ms: 1.06x slower                                                    |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.06x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 58.8 ms: 1.06x slower                                                   |
| pycparser                  | 1.19 sec                                               | 1.26 sec: 1.07x slower                                                  |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 69.4 ms: 1.07x slower                                                   |
| gc_traversal               | 4.01 ms                                                | 4.32 ms: 1.08x slower                                                   |
| django_template            | 33.5 ms                                                | 36.4 ms: 1.09x slower                                                   |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                   |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.10x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                   |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                                   |
| genshi_text                | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                   |
| float                      | 78.9 ms                                                | 89.8 ms: 1.14x slower                                                   |
| coverage                   | 78.8 ms                                                | 89.6 ms: 1.14x slower                                                   |
| 2to3                       | 264 ms                                                 | 302 ms: 1.14x slower                                                    |
| genshi_xml                 | 53.4 ms                                                | 61.3 ms: 1.15x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.38 ms: 1.15x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 93.2 ms: 1.15x slower                                                   |
| aiohttp                    | 1.12 ms                                                | 1.28 ms: 1.15x slower                                                   |
| html5lib                   | 64.8 ms                                                | 75.0 ms: 1.16x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 66.2 ms: 1.16x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.46 us: 1.19x slower                                                   |
| dask                       | 365 ms                                                 | 449 ms: 1.23x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 7.68 ms: 1.28x slower                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 140 ms: 1.29x slower                                                    |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                   |
| async_generators           | 374 ms                                                 | 488 ms: 1.31x slower                                                    |
| flaskblogging              | 7.28 ms                                                | 10.4 ms: 1.43x slower                                                   |
| docutils                   | 2.66 sec                                               | 3.83 sec: 1.44x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 2.23 ms: 1.55x slower                                                   |
| telco                      | 6.86 ms                                                | 170 ms: 24.84x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (2): bench_mp_pool, async_tree_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: djangocms, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 65.75% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x
# Results vs. 3.11.0

- fork: faster-cpython
- ref: lower_before
- machine: linux-x86_64
- commit hash: 68df0a5
- commit date: 2024-06-17
- overall geometric mean: 1.08x faster
- HPT reliability: 99.81%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                    |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                  |
| html5lib       | 64.8 ms                                                | 68.9 ms: 1.06x slower                                                   |
| tornado_http   | 98.1 ms                                                | 93.6 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 332 ms: 1.48x faster                                                    |
| async_tree_none            | 528 ms                                                 | 370 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 460 ms: 1.36x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 951 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 580 ms: 1.31x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 489 ms: 1.31x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 622 ms: 1.20x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.3 ms: 1.09x faster                                                   |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| float          | 78.9 ms                                                | 78.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.06x faster                                                    |
| regex_v8       | 22.9 ms                                                | 24.2 ms: 1.06x slower                                                   |
| regex_effbot   | 3.51 ms                                                | 3.79 ms: 1.08x slower                                                   |
| regex_dna      | 205 ms                                                 | 232 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 216 us: 1.12x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                    |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.7 us: 1.00x slower                                                   |
| unpickle_list        | 5.21 us                                                | 5.50 us: 1.05x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                   |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 86.3 ms: 1.06x slower                                                   |
| unpickle             | 13.8 us                                                | 14.8 us: 1.07x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.08 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.10 ms: 1.18x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.5 ms: 1.04x faster                                                   |
| django_template | 33.5 ms                                                | 34.4 ms: 1.03x slower                                                   |
| genshi_text     | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                   |
| mako            | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 166 us: 3.13x faster                                                    |
| generators                 | 74.9 ms                                                | 29.4 ms: 2.55x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                  |
| pylint                     | 476 ms                                                 | 316 ms: 1.51x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 332 ms: 1.48x faster                                                    |
| async_tree_none            | 528 ms                                                 | 370 ms: 1.43x faster                                                    |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 460 ms: 1.36x faster                                                    |
| deepcopy                   | 365 us                                                 | 270 us: 1.35x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 951 ms: 1.35x faster                                                    |
| deepcopy_memo              | 40.2 us                                                | 29.9 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 580 ms: 1.31x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 489 ms: 1.31x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.24 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 622 ms: 1.20x faster                                                    |
| chaos                      | 71.9 ms                                                | 60.4 ms: 1.19x faster                                                   |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                                    |
| deepcopy_reduce            | 3.22 us                                                | 2.78 us: 1.16x faster                                                   |
| pathlib                    | 18.5 ms                                                | 16.3 ms: 1.14x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.09 ms: 1.13x faster                                                   |
| nqueens                    | 87.9 ms                                                | 78.2 ms: 1.12x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 216 us: 1.12x faster                                                    |
| coroutines                 | 27.0 ms                                                | 24.3 ms: 1.11x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.62 us: 1.11x faster                                                   |
| richards_super             | 61.9 ms                                                | 56.1 ms: 1.10x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                    |
| nbody                      | 96.0 ms                                                | 88.3 ms: 1.09x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                   |
| logging_format             | 6.81 us                                                | 6.35 us: 1.07x faster                                                   |
| sympy_str                  | 297 ms                                                 | 280 ms: 1.06x faster                                                    |
| sympy_integrate            | 21.5 ms                                                | 20.2 ms: 1.06x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                  |
| regex_compile              | 141 ms                                                 | 134 ms: 1.06x faster                                                    |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                                    |
| mdp                        | 2.77 sec                                               | 2.63 sec: 1.06x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.80 ms: 1.05x faster                                                   |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                    |
| tornado_http               | 98.1 ms                                                | 93.6 ms: 1.05x faster                                                   |
| genshi_xml                 | 53.4 ms                                                | 51.5 ms: 1.04x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 74.0 ms: 1.04x faster                                                   |
| bench_thread_pool          | 834 us                                                 | 807 us: 1.03x faster                                                    |
| go                         | 149 ms                                                 | 145 ms: 1.03x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                    |
| sympy_expand               | 484 ms                                                 | 473 ms: 1.02x faster                                                    |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                  |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| scimark_monte_carlo        | 70.7 ms                                                | 69.1 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                    |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                    |
| scimark_lu                 | 116 ms                                                 | 114 ms: 1.02x faster                                                    |
| float                      | 78.9 ms                                                | 78.1 ms: 1.01x faster                                                   |
| fannkuch                   | 405 ms                                                 | 401 ms: 1.01x faster                                                    |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                    |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.55 sec: 1.01x faster                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 55.0 ms: 1.01x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                   |
| pickle_dict                | 34.6 us                                                | 34.7 us: 1.00x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 755 ms: 1.01x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 65.6 ms: 1.02x slower                                                   |
| json                       | 5.24 ms                                                | 5.35 ms: 1.02x slower                                                   |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                    |
| django_template            | 33.5 ms                                                | 34.4 ms: 1.03x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                    |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                    |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.04x slower                                                    |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                  |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                   |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                   |
| unpickle_list              | 5.21 us                                                | 5.50 us: 1.05x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                   |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 24.2 ms: 1.06x slower                                                   |
| html5lib                   | 64.8 ms                                                | 68.9 ms: 1.06x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 86.3 ms: 1.06x slower                                                   |
| unpickle                   | 13.8 us                                                | 14.8 us: 1.07x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.79 ms: 1.08x slower                                                   |
| scimark_fft                | 345 ms                                                 | 377 ms: 1.09x slower                                                    |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.10x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.08 us: 1.11x slower                                                   |
| regex_dna                  | 205 ms                                                 | 232 ms: 1.13x slower                                                    |
| pyflate                    | 434 ms                                                 | 492 ms: 1.14x slower                                                    |
| sqlite_synth               | 2.57 us                                                | 2.96 us: 1.15x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.10 ms: 1.18x slower                                                   |
| async_generators           | 374 ms                                                 | 442 ms: 1.18x slower                                                    |
| coverage                   | 78.8 ms                                                | 94.5 ms: 1.20x slower                                                   |
| telco                      | 6.86 ms                                                | 8.33 ms: 1.22x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                            |

Benchmark hidden because not significant (3): richards, dask, scimark_sparse_mat_mult
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (1) of results/bm-20240617-3.14.0a0-68df0a5/bm-20240617-linux-x86_64-faster%2dcpython-lower_before-3.14.0a0-68df0a5.json: bpe_tokeniser

# HPT report

- Reliability score: 99.81% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x
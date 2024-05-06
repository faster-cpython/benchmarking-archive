# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 313 ms: 1.18x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.93 ms: 1.18x slower                                                  |
| docutils       | 2.66 sec                                               | 3.14 sec: 1.18x slower                                                 |
| html5lib       | 64.8 ms                                                | 73.7 ms: 1.14x slower                                                  |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 365 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 475 ms: 1.32x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 996 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 501 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 638 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 639 ms: 1.17x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 196 ms: 1.01x slower                                                   |
| float          | 78.9 ms                                                | 91.6 ms: 1.16x slower                                                  |
| nbody          | 96.0 ms                                                | 117 ms: 1.22x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 205 ms                                                 | 219 ms: 1.07x slower                                                   |
| regex_effbot   | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.09x slower                                                  |
| regex_compile  | 141 ms                                                 | 190 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                                  |
| unpickle_list        | 5.21 us                                                | 5.12 us: 1.02x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 317 us: 1.01x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.5 us: 1.00x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 110 ms: 1.02x slower                                                   |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.15 us: 1.12x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 64.9 ms: 1.14x slower                                                  |
| tomli_loads          | 2.30 sec                                               | 2.63 sec: 1.14x slower                                                 |
| unpickle             | 13.8 us                                                | 15.9 us: 1.15x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 95.6 ms: 1.18x slower                                                  |
| unpickle_pure_python | 242 us                                                 | 334 us: 1.38x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.5 ms                                                | 26.2 ms: 1.17x slower                                                  |
| genshi_xml      | 53.4 ms                                                | 62.5 ms: 1.17x slower                                                  |
| mako            | 10.7 ms                                                | 13.4 ms: 1.26x slower                                                  |
| django_template | 33.5 ms                                                | 43.2 ms: 1.29x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 124 us: 4.18x faster                                                   |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                 |
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                   |
| pylint                     | 476 ms                                                 | 348 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 365 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 475 ms: 1.32x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 996 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 501 ms: 1.28x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.3 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 638 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 639 ms: 1.17x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.64 ms: 1.10x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                                  |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                   |
| unpickle_list              | 5.21 us                                                | 5.12 us: 1.02x faster                                                  |
| json                       | 5.24 ms                                                | 5.17 ms: 1.01x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 317 us: 1.01x faster                                                   |
| pathlib                    | 18.5 ms                                                | 18.4 ms: 1.01x faster                                                  |
| pickle_dict                | 34.6 us                                                | 34.5 us: 1.00x faster                                                  |
| pidigits                   | 194 ms                                                 | 196 ms: 1.01x slower                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 110 ms: 1.02x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                   |
| dask                       | 365 ms                                                 | 384 ms: 1.05x slower                                                   |
| mdp                        | 2.77 sec                                               | 2.93 sec: 1.05x slower                                                 |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.06x slower                                                   |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                  |
| richards_super             | 61.9 ms                                                | 65.7 ms: 1.06x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.42 us: 1.06x slower                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.87 ms: 1.07x slower                                                  |
| regex_dna                  | 205 ms                                                 | 219 ms: 1.07x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 181 ms: 1.07x slower                                                   |
| deepcopy                   | 365 us                                                 | 392 us: 1.07x slower                                                   |
| logging_simple             | 6.22 us                                                | 6.69 us: 1.08x slower                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.54 ms: 1.08x slower                                                  |
| thrift                     | 784 us                                                 | 848 us: 1.08x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                  |
| comprehensions             | 23.6 us                                                | 25.6 us: 1.08x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.09x slower                                                  |
| logging_format             | 6.81 us                                                | 7.41 us: 1.09x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 910 us: 1.09x slower                                                   |
| pycparser                  | 1.19 sec                                               | 1.31 sec: 1.10x slower                                                 |
| deltablue                  | 3.92 ms                                                | 4.33 ms: 1.10x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 23.8 ms: 1.11x slower                                                  |
| sympy_str                  | 297 ms                                                 | 331 ms: 1.11x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.34 ms: 1.12x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.12x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.15 us: 1.12x slower                                                  |
| chaos                      | 71.9 ms                                                | 80.8 ms: 1.12x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.67 ms: 1.13x slower                                                  |
| meteor_contest             | 109 ms                                                 | 123 ms: 1.13x slower                                                   |
| sympy_expand               | 484 ms                                                 | 548 ms: 1.13x slower                                                   |
| sqlglot_normalize          | 113 ms                                                 | 128 ms: 1.13x slower                                                   |
| html5lib                   | 64.8 ms                                                | 73.7 ms: 1.14x slower                                                  |
| raytrace                   | 309 ms                                                 | 352 ms: 1.14x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 64.9 ms: 1.14x slower                                                  |
| tomli_loads                | 2.30 sec                                               | 2.63 sec: 1.14x slower                                                 |
| unpickle                   | 13.8 us                                                | 15.9 us: 1.15x slower                                                  |
| float                      | 78.9 ms                                                | 91.6 ms: 1.16x slower                                                  |
| genshi_text                | 22.5 ms                                                | 26.2 ms: 1.17x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 75.4 ms: 1.17x slower                                                  |
| genshi_xml                 | 53.4 ms                                                | 62.5 ms: 1.17x slower                                                  |
| richards                   | 49.8 ms                                                | 58.3 ms: 1.17x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 95.6 ms: 1.18x slower                                                  |
| docutils                   | 2.66 sec                                               | 3.14 sec: 1.18x slower                                                 |
| 2to3                       | 264 ms                                                 | 313 ms: 1.18x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.93 ms: 1.18x slower                                                  |
| mypy2                      | 686 ms                                                 | 819 ms: 1.19x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 66.2 ms: 1.20x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 3.08 us: 1.20x slower                                                  |
| crypto_pyaes               | 76.7 ms                                                | 93.0 ms: 1.21x slower                                                  |
| deepcopy_memo              | 40.2 us                                                | 48.9 us: 1.22x slower                                                  |
| nbody                      | 96.0 ms                                                | 117 ms: 1.22x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| coverage                   | 78.8 ms                                                | 96.9 ms: 1.23x slower                                                  |
| mako                       | 10.7 ms                                                | 13.4 ms: 1.26x slower                                                  |
| django_template            | 33.5 ms                                                | 43.2 ms: 1.29x slower                                                  |
| async_generators           | 374 ms                                                 | 485 ms: 1.30x slower                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 92.3 ms: 1.31x slower                                                  |
| go                         | 149 ms                                                 | 194 ms: 1.31x slower                                                   |
| fannkuch                   | 405 ms                                                 | 537 ms: 1.33x slower                                                   |
| scimark_sor                | 121 ms                                                 | 162 ms: 1.33x slower                                                   |
| regex_compile              | 141 ms                                                 | 190 ms: 1.34x slower                                                   |
| unpickle_pure_python       | 242 us                                                 | 334 us: 1.38x slower                                                   |
| telco                      | 6.86 ms                                                | 9.47 ms: 1.38x slower                                                  |
| nqueens                    | 87.9 ms                                                | 125 ms: 1.42x slower                                                   |
| pyflate                    | 434 ms                                                 | 633 ms: 1.46x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 172 ms: 1.47x slower                                                   |
| pprint_pformat             | 1.55 sec                                               | 2.31 sec: 1.49x slower                                                 |
| hexiom                     | 6.89 ms                                                | 10.3 ms: 1.49x slower                                                  |
| pprint_safe_repr           | 747 ms                                                 | 1.12 sec: 1.50x slower                                                 |
| scimark_fft                | 345 ms                                                 | 543 ms: 1.57x slower                                                   |
| spectral_norm              | 108 ms                                                 | 203 ms: 1.87x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (2): djangocms, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.03x
# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: stackref_all
- machine: linux-x86_64
- commit hash: 6a6bae2
- commit date: 2024-06-04
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 406 ms: 1.54x slower                                                    |
| docutils       | 2.66 sec                                               | 3.44 sec: 1.29x slower                                                  |
| html5lib       | 64.8 ms                                                | 102 ms: 1.57x slower                                                    |
| tornado_http   | 98.1 ms                                                | 139 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                  | 1.45x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 979 ms: 1.31x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 536 ms: 1.17x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 427 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 678 ms: 1.12x faster                                                    |
| async_tree_none            | 528 ms                                                 | 472 ms: 1.12x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 586 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 732 ms: 1.02x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.17x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 187 ms: 1.04x faster                                                    |
| float          | 78.9 ms                                                | 141 ms: 1.78x slower                                                    |
| nbody          | 96.0 ms                                                | 234 ms: 2.44x slower                                                    |
| Geometric mean | (ref)                                                  | 1.61x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.48 ms: 1.01x faster                                                   |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                    |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                   |
| regex_compile  | 141 ms                                                 | 227 ms: 1.61x slower                                                    |
| Geometric mean | (ref)                                                  | 1.18x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 164 ms                                                 | 154 ms: 1.06x faster                                                    |
| json_dumps           | 13.3 ms                                                | 14.2 ms: 1.07x slower                                                   |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                   |
| pickle_list          | 4.59 us                                                | 4.90 us: 1.07x slower                                                   |
| json_loads           | 29.2 us                                                | 31.8 us: 1.09x slower                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 118 ms: 1.09x slower                                                    |
| unpickle_list        | 5.21 us                                                | 5.73 us: 1.10x slower                                                   |
| unpickle             | 13.8 us                                                | 16.2 us: 1.17x slower                                                   |
| pickle_dict          | 34.6 us                                                | 41.1 us: 1.19x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 115 ms: 1.41x slower                                                    |
| tomli_loads          | 2.30 sec                                               | 3.38 sec: 1.47x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 92.8 ms: 1.63x slower                                                   |
| unpickle_pure_python | 242 us                                                 | 423 us: 1.75x slower                                                    |
| pickle_pure_python   | 320 us                                                 | 611 us: 1.91x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.25x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 9.18 ms: 1.53x slower                                                   |
| python_startup         | 8.56 ms                                                | 13.7 ms: 1.60x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 86.7 ms: 1.62x slower                                                   |
| genshi_text     | 22.5 ms                                                | 41.6 ms: 1.85x slower                                                   |
| django_template | 33.5 ms                                                | 62.9 ms: 1.87x slower                                                   |
| mako            | 10.7 ms                                                | 21.6 ms: 2.02x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.84x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 266 us: 1.95x faster                                                    |
| generators                 | 74.9 ms                                                | 39.1 ms: 1.92x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 2.13 sec: 1.46x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 600 ms: 1.46x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 2.78 ms: 1.44x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 979 ms: 1.31x faster                                                    |
| bench_mp_pool              | 24.0 ms                                                | 20.4 ms: 1.18x faster                                                   |
| pylint                     | 476 ms                                                 | 405 ms: 1.17x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 536 ms: 1.17x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 427 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 678 ms: 1.12x faster                                                    |
| async_tree_none            | 528 ms                                                 | 472 ms: 1.12x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 586 ms: 1.09x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 154 ms: 1.06x faster                                                    |
| create_gc_cycles           | 1.43 ms                                                | 1.37 ms: 1.05x faster                                                   |
| pidigits                   | 194 ms                                                 | 187 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 732 ms: 1.02x faster                                                    |
| regex_effbot               | 3.51 ms                                                | 3.48 ms: 1.01x faster                                                   |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                    |
| pathlib                    | 18.5 ms                                                | 19.7 ms: 1.06x slower                                                   |
| json_dumps                 | 13.3 ms                                                | 14.2 ms: 1.07x slower                                                   |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                   |
| pickle_list                | 4.59 us                                                | 4.90 us: 1.07x slower                                                   |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                    |
| json_loads                 | 29.2 us                                                | 31.8 us: 1.09x slower                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 118 ms: 1.09x slower                                                    |
| unpickle_list              | 5.21 us                                                | 5.73 us: 1.10x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                   |
| json                       | 5.24 ms                                                | 5.98 ms: 1.14x slower                                                   |
| unpickle                   | 13.8 us                                                | 16.2 us: 1.17x slower                                                   |
| pickle_dict                | 34.6 us                                                | 41.1 us: 1.19x slower                                                   |
| coroutines                 | 27.0 ms                                                | 33.0 ms: 1.22x slower                                                   |
| mdp                        | 2.77 sec                                               | 3.42 sec: 1.23x slower                                                  |
| comprehensions             | 23.6 us                                                | 29.7 us: 1.26x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 3.25 us: 1.26x slower                                                   |
| docutils                   | 2.66 sec                                               | 3.44 sec: 1.29x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 29.5 ms: 1.38x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 89.0 ms: 1.38x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.94 ms: 1.38x slower                                                   |
| nqueens                    | 87.9 ms                                                | 122 ms: 1.39x slower                                                    |
| pycparser                  | 1.19 sec                                               | 1.65 sec: 1.39x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 115 ms: 1.41x slower                                                    |
| meteor_contest             | 109 ms                                                 | 154 ms: 1.41x slower                                                    |
| tornado_http               | 98.1 ms                                                | 139 ms: 1.42x slower                                                    |
| telco                      | 6.86 ms                                                | 9.83 ms: 1.43x slower                                                   |
| scimark_fft                | 345 ms                                                 | 506 ms: 1.47x slower                                                    |
| tomli_loads                | 2.30 sec                                               | 3.38 sec: 1.47x slower                                                  |
| sympy_str                  | 297 ms                                                 | 438 ms: 1.47x slower                                                    |
| async_generators           | 374 ms                                                 | 565 ms: 1.51x slower                                                    |
| crypto_pyaes               | 76.7 ms                                                | 117 ms: 1.52x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 9.18 ms: 1.53x slower                                                   |
| 2to3                       | 264 ms                                                 | 406 ms: 1.54x slower                                                    |
| fannkuch                   | 405 ms                                                 | 626 ms: 1.54x slower                                                    |
| sympy_sum                  | 169 ms                                                 | 262 ms: 1.55x slower                                                    |
| html5lib                   | 64.8 ms                                                | 102 ms: 1.57x slower                                                    |
| python_startup             | 8.56 ms                                                | 13.7 ms: 1.60x slower                                                   |
| sympy_expand               | 484 ms                                                 | 778 ms: 1.61x slower                                                    |
| regex_compile              | 141 ms                                                 | 227 ms: 1.61x slower                                                    |
| sqlglot_normalize          | 113 ms                                                 | 182 ms: 1.61x slower                                                    |
| genshi_xml                 | 53.4 ms                                                | 86.7 ms: 1.62x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 92.8 ms: 1.63x slower                                                   |
| richards_super             | 61.9 ms                                                | 101 ms: 1.63x slower                                                    |
| deepcopy                   | 365 us                                                 | 598 us: 1.64x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 91.4 ms: 1.65x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 5.39 us: 1.68x slower                                                   |
| richards                   | 49.8 ms                                                | 83.6 ms: 1.68x slower                                                   |
| deepcopy_memo              | 40.2 us                                                | 69.8 us: 1.74x slower                                                   |
| unpickle_pure_python       | 242 us                                                 | 423 us: 1.75x slower                                                    |
| logging_simple             | 6.22 us                                                | 11.1 us: 1.78x slower                                                   |
| float                      | 78.9 ms                                                | 141 ms: 1.78x slower                                                    |
| logging_format             | 6.81 us                                                | 12.2 us: 1.79x slower                                                   |
| chaos                      | 71.9 ms                                                | 129 ms: 1.80x slower                                                    |
| spectral_norm              | 108 ms                                                 | 195 ms: 1.81x slower                                                    |
| logging_silent             | 111 ns                                                 | 203 ns: 1.83x slower                                                    |
| pprint_pformat             | 1.55 sec                                               | 2.85 sec: 1.83x slower                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 130 ms: 1.84x slower                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 3.22 ms: 1.84x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 1.38 sec: 1.84x slower                                                  |
| hexiom                     | 6.89 ms                                                | 12.7 ms: 1.85x slower                                                   |
| genshi_text                | 22.5 ms                                                | 41.6 ms: 1.85x slower                                                   |
| django_template            | 33.5 ms                                                | 62.9 ms: 1.87x slower                                                   |
| pyflate                    | 434 ms                                                 | 813 ms: 1.87x slower                                                    |
| pickle_pure_python         | 320 us                                                 | 611 us: 1.91x slower                                                    |
| sqlglot_parse              | 1.43 ms                                                | 2.74 ms: 1.91x slower                                                   |
| mako                       | 10.7 ms                                                | 21.6 ms: 2.02x slower                                                   |
| raytrace                   | 309 ms                                                 | 628 ms: 2.03x slower                                                    |
| scimark_lu                 | 116 ms                                                 | 254 ms: 2.18x slower                                                    |
| go                         | 149 ms                                                 | 329 ms: 2.21x slower                                                    |
| deltablue                  | 3.92 ms                                                | 8.80 ms: 2.24x slower                                                   |
| scimark_sor                | 121 ms                                                 | 274 ms: 2.25x slower                                                    |
| nbody                      | 96.0 ms                                                | 234 ms: 2.44x slower                                                    |
| bench_thread_pool          | 834 us                                                 | 3.15 ms: 3.78x slower                                                   |
| coverage                   | 78.8 ms                                                | 802 ms: 10.19x slower                                                   |
| thrift                     | 784 us                                                 | 13.6 ms: 17.35x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.42x slower                                                            |
Ignored benchmarks (10) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dask, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x
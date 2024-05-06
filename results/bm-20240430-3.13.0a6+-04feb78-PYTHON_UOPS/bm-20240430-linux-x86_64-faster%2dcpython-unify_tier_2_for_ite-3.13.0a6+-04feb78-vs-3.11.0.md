# Results vs. 3.11.0

- fork: faster-cpython
- ref: unify_tier_2_for_ite
- machine: linux-x86_64
- commit hash: 04feb78
- commit date: 2024-04-30
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 321 ms: 1.22x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.94 ms: 1.19x slower                                                            |
| docutils       | 2.66 sec                                               | 3.19 sec: 1.20x slower                                                           |
| html5lib       | 64.8 ms                                                | 76.3 ms: 1.18x slower                                                            |
| tornado_http   | 98.1 ms                                                | 104 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 373 ms: 1.42x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 958 ms: 1.35x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 964 ms: 1.34x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 499 ms: 1.28x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 620 ms: 1.23x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 213 ms: 1.10x slower                                                             |
| float          | 78.9 ms                                                | 91.9 ms: 1.16x slower                                                            |
| nbody          | 96.0 ms                                                | 125 ms: 1.30x slower                                                             |
| Geometric mean | (ref)                                                  | 1.18x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                            |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                            |
| regex_compile  | 141 ms                                                 | 181 ms: 1.28x slower                                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 153 ms: 1.07x faster                                                             |
| json_loads           | 29.2 us                                                | 27.7 us: 1.06x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 321 us: 1.00x slower                                                             |
| unpickle_list        | 5.21 us                                                | 5.28 us: 1.01x slower                                                            |
| pickle_dict          | 34.6 us                                                | 35.2 us: 1.02x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 111 ms: 1.03x slower                                                             |
| pickle_list          | 4.59 us                                                | 5.02 us: 1.10x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.54 sec: 1.10x slower                                                           |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| unpickle_pure_python | 242 us                                                 | 286 us: 1.18x slower                                                             |
| xml_etree_process    | 56.9 ms                                                | 67.5 ms: 1.19x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 96.3 ms: 1.19x slower                                                            |
| unpickle             | 13.8 us                                                | 16.5 us: 1.19x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.17 ms: 1.19x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 33.5 ms                                                | 40.7 ms: 1.21x slower                                                            |
| mako            | 10.7 ms                                                | 14.0 ms: 1.31x slower                                                            |
| genshi_xml      | 53.4 ms                                                | 70.8 ms: 1.32x slower                                                            |
| genshi_text     | 22.5 ms                                                | 31.2 ms: 1.39x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 190 us: 2.74x faster                                                             |
| generators                 | 74.9 ms                                                | 31.2 ms: 2.40x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 528 ms: 1.66x faster                                                             |
| async_tree_none            | 528 ms                                                 | 373 ms: 1.42x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 958 ms: 1.35x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 964 ms: 1.34x faster                                                             |
| pylint                     | 476 ms                                                 | 365 ms: 1.31x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 499 ms: 1.28x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 620 ms: 1.23x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                             |
| coroutines                 | 27.0 ms                                                | 24.3 ms: 1.11x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 153 ms: 1.07x faster                                                             |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.06x faster                                                            |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                             |
| pathlib                    | 18.5 ms                                                | 18.2 ms: 1.02x faster                                                            |
| json                       | 5.24 ms                                                | 5.16 ms: 1.01x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 321 us: 1.00x slower                                                             |
| gc_traversal               | 4.01 ms                                                | 4.06 ms: 1.01x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.28 us: 1.01x slower                                                            |
| mdp                        | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| pickle_dict                | 34.6 us                                                | 35.2 us: 1.02x slower                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 111 ms: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                             |
| logging_simple             | 6.22 us                                                | 6.44 us: 1.04x slower                                                            |
| logging_format             | 6.81 us                                                | 7.09 us: 1.04x slower                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.82 ms: 1.04x slower                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.49 ms: 1.04x slower                                                            |
| comprehensions             | 23.6 us                                                | 24.6 us: 1.04x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.38 us: 1.05x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                            |
| tornado_http               | 98.1 ms                                                | 104 ms: 1.06x slower                                                             |
| dask                       | 365 ms                                                 | 386 ms: 1.06x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 179 ms: 1.06x slower                                                             |
| thrift                     | 784 us                                                 | 831 us: 1.06x slower                                                             |
| deepcopy                   | 365 us                                                 | 389 us: 1.07x slower                                                             |
| richards_super             | 61.9 ms                                                | 66.5 ms: 1.08x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.28 sec: 1.08x slower                                                           |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                             |
| raytrace                   | 309 ms                                                 | 334 ms: 1.08x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                            |
| deltablue                  | 3.92 ms                                                | 4.29 ms: 1.09x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 912 us: 1.09x slower                                                             |
| chaos                      | 71.9 ms                                                | 78.6 ms: 1.09x slower                                                            |
| pidigits                   | 194 ms                                                 | 213 ms: 1.10x slower                                                             |
| pickle_list                | 4.59 us                                                | 5.02 us: 1.10x slower                                                            |
| tomli_loads                | 2.30 sec                                               | 2.54 sec: 1.10x slower                                                           |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| sympy_str                  | 297 ms                                                 | 332 ms: 1.12x slower                                                             |
| meteor_contest             | 109 ms                                                 | 122 ms: 1.12x slower                                                             |
| gunicorn                   | 1.20 ms                                                | 1.35 ms: 1.13x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                                            |
| sympy_integrate            | 21.5 ms                                                | 24.2 ms: 1.13x slower                                                            |
| deepcopy_memo              | 40.2 us                                                | 45.5 us: 1.13x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 129 ms: 1.14x slower                                                             |
| sympy_expand               | 484 ms                                                 | 561 ms: 1.16x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 75.1 ms: 1.16x slower                                                            |
| float                      | 78.9 ms                                                | 91.9 ms: 1.16x slower                                                            |
| crypto_pyaes               | 76.7 ms                                                | 89.6 ms: 1.17x slower                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 65.0 ms: 1.17x slower                                                            |
| html5lib                   | 64.8 ms                                                | 76.3 ms: 1.18x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 3.03 us: 1.18x slower                                                            |
| unpickle_pure_python       | 242 us                                                 | 286 us: 1.18x slower                                                             |
| chameleon                  | 6.70 ms                                                | 7.94 ms: 1.19x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 67.5 ms: 1.19x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.97 ms: 1.19x slower                                                            |
| fannkuch                   | 405 ms                                                 | 481 ms: 1.19x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 96.3 ms: 1.19x slower                                                            |
| coverage                   | 78.8 ms                                                | 93.6 ms: 1.19x slower                                                            |
| unpickle                   | 13.8 us                                                | 16.5 us: 1.19x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.17 ms: 1.19x slower                                                            |
| docutils                   | 2.66 sec                                               | 3.19 sec: 1.20x slower                                                           |
| richards                   | 49.8 ms                                                | 59.7 ms: 1.20x slower                                                            |
| django_template            | 33.5 ms                                                | 40.7 ms: 1.21x slower                                                            |
| 2to3                       | 264 ms                                                 | 321 ms: 1.22x slower                                                             |
| mypy2                      | 686 ms                                                 | 842 ms: 1.23x slower                                                             |
| nqueens                    | 87.9 ms                                                | 109 ms: 1.24x slower                                                             |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 89.5 ms: 1.27x slower                                                            |
| spectral_norm              | 108 ms                                                 | 137 ms: 1.27x slower                                                             |
| async_generators           | 374 ms                                                 | 476 ms: 1.27x slower                                                             |
| regex_compile              | 141 ms                                                 | 181 ms: 1.28x slower                                                             |
| pprint_pformat             | 1.55 sec                                               | 2.00 sec: 1.28x slower                                                           |
| scimark_fft                | 345 ms                                                 | 445 ms: 1.29x slower                                                             |
| pprint_safe_repr           | 747 ms                                                 | 965 ms: 1.29x slower                                                             |
| nbody                      | 96.0 ms                                                | 125 ms: 1.30x slower                                                             |
| mako                       | 10.7 ms                                                | 14.0 ms: 1.31x slower                                                            |
| scimark_sor                | 121 ms                                                 | 159 ms: 1.31x slower                                                             |
| genshi_xml                 | 53.4 ms                                                | 70.8 ms: 1.32x slower                                                            |
| telco                      | 6.86 ms                                                | 9.32 ms: 1.36x slower                                                            |
| go                         | 149 ms                                                 | 203 ms: 1.37x slower                                                             |
| pyflate                    | 434 ms                                                 | 595 ms: 1.37x slower                                                             |
| genshi_text                | 22.5 ms                                                | 31.2 ms: 1.39x slower                                                            |
| hexiom                     | 6.89 ms                                                | 9.77 ms: 1.42x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 168 ms: 1.44x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                                     |

Benchmark hidden because not significant (2): djangocms, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.04x